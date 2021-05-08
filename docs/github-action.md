# Automatic Site Deployment with Github Action
This is a configuration which allows your documentation from github to auto-deploy to the github pages.

???+ example "Why do I need this?"
    Let me give you an example, for this documentation it is hosted at https://frinzekt.github.io/mkdocs-frinze-template/ . If this thing is configured, then whenever you modify the github repository, it automatically redeploys in github pages.

## How do I do this?

If you look closely in the repository, there is a file `.github/workflows/main.yml`. Copy this file over to you repository. The content of it is roughly like below. Note that you have to change 2 lines highlighted to the path of your documentation. 

??? example "Example of Path that you will have to change"
    If in the scenario that your repository is just documentation, which means that your `mkdocs.yml` file is in the root, then you don't have to change anything.

    However, there are cases where you have a monorepo - a type of repository that contains multiple files such as for example in a software project, there are the documentation files, and source code files. It is quite common to have a file structure that looks like this:

    ```
    frontend/
        ...
    backend/
        ...
    mkdocs/
        mkdocs.yml    # The configuration file.
        docs/
            index.md  # The documentation homepage.
            ...       # Other markdown pages, images and other files.
    ```

    This means that you will have to change the one highlighted. From the example above here, the correct lines changes are:

    `key: ${{ runner.os }}-pip-${{ hashFiles('**/requirements.txt') }}` to `key: ${{ runner.os }}-pip-${{ hashFiles('**/mkdocs/requirements.txt') }}`

    and 

    `python3 -m pip install -r ./requirements.txt` to `python3 -m pip install -r ./mkdocs/requirements.txt`

```yml hl_lines="36 40"
# Workflow for deploying to github
name: Publish docs via GitHub Pages
on:
  push:
    branches:
      - master
      - main
      - mkdocs-experimental
  workflow_dispatch:

jobs:
  deploy:
    name: Deploy docs
    runs-on: ubuntu-latest
    steps:
      - name: Checkout main
        uses: actions/checkout@v2

      - name: Setup Python
        uses: actions/setup-python@v2
        with:
          python-version: '3.8'

      - name: Upgrade pip
        run: |
          # install pip=>20.1 to use "pip cache dir"
          python3 -m pip install --upgrade pip
      - name: Get pip cache dir
        id: pip-cache
        run: echo "::set-output name=dir::$(pip cache dir)"

      - name: Cache dependencies
        uses: actions/cache@v2
        with:
          path: ${{ steps.pip-cache.outputs.dir }}
          key: ${{ runner.os }}-pip-${{ hashFiles('**/requirements.txt') }}
          restore-keys: |
            ${{ runner.os }}-pip-
      - name: Install dependencies
        run: python3 -m pip install -r ./requirements.txt

      - run: mkdocs build
        env: 
          ENABLE_PDF_EXPORT: 1

      - name: Deploy
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./site
```

## Custom Domain Name

In the scenario that you like a custom domain name such as https://www.tutorial-mkdocs.systemhealthlab.com , follow this [documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages).

tldr (too long didn't read) instructions:
1. Go to the domain registar, in my case Cloudflare
2. Register a "CNAME" of the domain/subdomain going towards `<organisation/githubname>.github.io` (eg. `uwasystemhealth.github.io`)
3. Add a `CNAME` file with the name of the domain/subdomain in the `/docs` folder
4. Give the `CNAME` file a content of the subdomain name (eg. `tutorial-mkdocs.systemhealthlab.com`)