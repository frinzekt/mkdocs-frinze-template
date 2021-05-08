# Welcome to MkDocs Frinze Template
This is my template that I have created while I was working for a cool workplaces namely [Lotterywest](https://www.lotterywest.wa.gov.au/) and [UWA System Health Lab](http://systemhealthlab.com/). This is a template that contains extensions that are very nice to have when you just want a standard documentation for anything!

For full documentation visit:

- [mkdocs.org](https://www.mkdocs.org) for the generic MkDocs
- [PyMdown Extensions](https://facelessuser.github.io/pymdown-extensions/) for the different extensions that are installed
- [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) for the customisation of the web server documentation.

## How easy is this to deploy?

1. Fork / Clone This [Repo](https://github.com/frinzekt/mkdocs-frinze-template/tree/main)
   1. Follow the [installation](#installation)
2. Delete the markdown files here and replace it with your own
3. Maybe put your own Nav in the `mkdocs.yml` file
4. Deploy somewhere ! (easist way Github Pages see [here](#commands))
   
## What inspired me to do this?
I have seen that a lot of the documentation is really scattered for Mkdocs. Like the documentation is good and there are a lot of them, but all I really wanted was a generic template with most of the extensions that I will need without being caught up on which one to pick, and so on; so, I ended up creating this which aims to give you a very easy way to start your documentation. In addition, there was some hussle sometimes, in trying to figure out why some extensions aren't working, and it is just frustrating and time-consuming.

Just erase those markdown files in the `/docs` file, and you can get started.

## Installation
Install this preferably in your global environment because this is just a code generator and so.
```
pip install -r requirements.txt
```
## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server. Very helpful when you want to take a look at the docs before deploying.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.
* `mkdocs gh-deploy` - Deploy in github pages

## Project layout
```
    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.
```

## Extending this template

I made this template to be simple such that it gives you a brief overview of how you would be writing your documentation with a few configuration. This is the type of documentation that you just build on top of.

If in the scenario that you feel that I missed that is essential to be in the template, please feel free to give this repository a pull request. However, if you feel that you would like to extend this template much more, I would highly recommend to visit the original [Mkdocs Material Documentation](https://squidfunk.github.io/mkdocs-material/customization/).
