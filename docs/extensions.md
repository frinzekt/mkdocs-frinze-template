# Extensions Installed Overview

This is a VERY VERY small overview to what you can do with this. I will just highlight some of them, because those are the only documentation syntax that I commonly use and usually remember.

## Admonitions
These are kind of those fancy boxes that you usually in cool Science Books that adds extra information.

!!! note
    As you can see this box, is very attractive.

    The syntax for this is:
    ```markdown
    !!! note
    As you can see this box, is very attractive.
    ```

!!! note "What If You want a different Title"
    The syntax for this is:
    ```markdown
    !!! note "What If You want a different Title"
    As you can see this box, is very attractive.
    ```


### Icons
More info [here](https://squidfunk.github.io/mkdocs-material/reference/admonitions/#supported-types)

You can also change these icons by changing the first word after `!!!` or `???`.

`note`{: #note }, `seealso`

:   !!! note

        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et
        euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo
        purus auctor massa, nec semper lorem quam in massa.

`abstract`{: #abstract }, `summary`, `tldr`

:   !!! abstract

        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et
        euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo
        purus auctor massa, nec semper lorem quam in massa.

`info`{: #info }, `todo`

:   !!! info

        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et
        euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo
        purus auctor massa, nec semper lorem quam in massa.

`tip`{: #tip }, `hint`, `important`

:   !!! tip

        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et
        euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo
        purus auctor massa, nec semper lorem quam in massa.

`success`{: #success }, `check`, `done`

:   !!! success

        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et
        euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo
        purus auctor massa, nec semper lorem quam in massa.

`question`{: #question }, `help`, `faq`

:   !!! question

        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et
        euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo
        purus auctor massa, nec semper lorem quam in massa.

`warning`{: #warning }, `caution`, `attention`

:   !!! warning

        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et
        euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo
        purus auctor massa, nec semper lorem quam in massa.

`failure`{: #failure }, `fail`, `missing`

:   !!! failure

        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et
        euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo
        purus auctor massa, nec semper lorem quam in massa.

`danger`{: #danger }, `error`

:   !!! danger

        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et
        euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo
        purus auctor massa, nec semper lorem quam in massa.

`bug`{: #bug }

:   !!! bug

        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et
        euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo
        purus auctor massa, nec semper lorem quam in massa.

`example`{: #example }

:   !!! example

        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et
        euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo
        purus auctor massa, nec semper lorem quam in massa.

`quote`{: #quote }, `cite`

:   !!! quote

        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et
        euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo
        purus auctor massa, nec semper lorem quam in massa.

### Collapsible Block
More info [here](https://squidfunk.github.io/mkdocs-material/reference/admonitions/)

If things are getting a little bit crowded, why not make some of them collapsible?

??? Example "Example of a More Complex Documentation"
    Here is the basic idea of bubble sort!
    ```python
    def bubble_sort(items):
        for i in range(len(items)):
            for j in range(len(items) - 1 - i):
                if items[j] > items[j + 1]:
                    items[j], items[j + 1] = items[j + 1], items[j]
    ```

??? Example "The Syntax for the Example Above"
    ```markdown
        ??? Example "Example of a More Complex Documentation"
        Here is the basic idea of bubble sort!
        ```python
        def bubble_sort(items):
            for i in range(len(items)):
                for j in range(len(items) - 1 - i):
                    if items[j] > items[j + 1]:
                        items[j], items[j + 1] = items[j + 1], items[j]
        ```
    ```

## Code Highlight
This is powered by codehilite. Whenever, you need code, this is the one that makes it pretty.

*For example:*
``` python
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

??? Example "Syntax of the Example Above"
    ```markdown
        ``` python linenums="1"
        def bubble_sort(items):
            for i in range(len(items)):
                for j in range(len(items) - 1 - i):
                    if items[j] > items[j + 1]:
                        items[j], items[j + 1] = items[j + 1], items[j]
        ```
    ```

### Highlight Specific Code Lines
What if I want to show some cool lines?
I could highlight which specific line number should be highlighted.

``` python hl_lines="2 3"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

??? Example "Syntax of the Example Above"
    ```markdown
        ``` python hl_lines="2 3"
        def bubble_sort(items):
            for i in range(len(items)):
                for j in range(len(items) - 1 - i):
                    if items[j] > items[j + 1]:
                        items[j], items[j + 1] = items[j + 1], items[j]
        ```
    ```

## Latex / Math Symbol Renderer
This is for math nerds that needs some Maths in their documentation. More info on Latex [here](http://www.icl.utk.edu/~mgates3/docs/latex.pdf).

For example, the Pythagoras Theorem
$$ a^2 + b^2 = c^2 $$

??? Example "Syntax of the Example Above"
    ```latex
    $$ a^2 + b^2 = c^2 $$
    ```

### Inline Latex
According to the results with the p-value $p < 0.05$, it means that we will reject the null Hypothesis $H_0$, and that there is a significant difference in the means.

## Footnotes
*Woah woah woah! Getting a little bit nerdy referencer here!*

"You can tell that I don't know much about referencing"[^1]. If you click this shiny number, it takes you to the bottom of the page where the reference is.

[^1]:
    Book of Wisdom - John Doe

??? Example "Syntax of the Example Above"
    ```markdown
    "You can tell that I don't know much about referencing"[^1]

    [^1]:
    Book of Wisdom - John Doe
    ```

## Content Tabs
Very useful for when you need one or the other.

For example, when dealing with multiple programming languages.

=== "C"

    ``` c
    #include <stdio.h>

    int main(void) {
      printf("Hello world!\n");
      return 0;
    }
    ```

=== "C++"

    ``` c++
    #include <iostream>

    int main(void) {
      std::cout << "Hello world!" << std::endl;
      return 0;
    }
    ```

??? Example "Syntax of Above"
    ```markdown
        === "C"

            ``` c
            #include <stdio.h>

            int main(void) {
            printf("Hello world!\n");
            return 0;
            }
            ```

        === "C++"

            ``` c++
            #include <iostream>

            int main(void) {
            std::cout << "Hello world!" << std::endl;
            return 0;
            }
            ```
    ```

## Icons and Emoji
Just worth mentioning, not too sure if you're going to use it.

- :material-account-circle: – `.icons/material/account-circle.svg`
- :fontawesome-regular-laugh-wink: – `.icons/fontawesome/regular/laugh-wink.svg`
- :octicons-octoface-16: – `.icons/octicons/octoface-16.svg`

??? Example "Syntax of Above"
    ```
    - :material-account-circle: – `.icons/material/account-circle.svg`
    - :fontawesome-regular-laugh-wink: – `.icons/fontawesome/regular/laugh-wink.svg`
    - :octicons-octoface-16: – `.icons/octicons/octoface-16.svg`
    ```

## Images
Can be done with Markdown or HTML.

### Image Captioning
<figure>
  <img src="../images/docs.png" width="100" />
  <figcaption>The Logo that Daphne from Coders for Causes gave me</figcaption>
</figure>

??? Example "Syntax of Above"
    ```html
    <figure>
        <img src="../images/docs.png" width="100" />
        <figcaption>The Logo that Daphne from Coders for Causes gave me</figcaption>
    </figure>
    ```

### Image Alignment

![Placeholder](https://dummyimage.com/600x400/f5f5f5/aaaaaa&text=–%20Image%20–){: align=left width=300 }

This is for when you have paragraphs and some text, but you really wanted those fancy images on the side. You can either say `left` or `right`. Now Let me just fill this with some random words so that the image doesn't look to weird.

<br/>

??? Example "Syntax Above"
    ```markdown
    ![Placeholder](https://dummyimage.com/600x400/f5f5f5/aaaaaa&text=–%20Image%20–){: align=left width=300 }

    This is for when you have paragraphs and some text, but you really wanted those fancy images on the side. You can either say `left` or `right`. Now Let me just fill this with some random words so that the image doesn't look to weird.
    ```

## Graph In Markdown / Mermaid Markdown
More Information [here](https://mermaidjs.github.io/).

What if you really just want to create some fancy graphs, but you really can't be bothered to:

1. Load some other software
2. Draw this graph that you wanted to show
3. Save this graph that you want to show
4. Upload this graph somewhere
5. Link this image back to this documentation

Like there are just soooo many steps.

Introducing **mermaid markdown**.

```mermaid
graph TD
    A --> B & C
    B --> C
```

??? Example "Syntax for Above"
    ```markdown
        ```mermaid
        graph TD
            A --> B & C
            B --> C
        ```
    ```

How about more complex ones? Is this complex enough for your

```mermaid
graph TD
    A[Hard] -->|Text| B(Round)
    B --> C{Decision}
    C -->|One| D[Result 1]
    C -->|Two| E[Result 2]
```

??? Example "Syntax for Above"
    ```markdown
        ```mermaid
        graph TD
            A[Hard] -->|Text| B(Round)
            B --> C{Decision}
            C -->|One| D[Result 1]
            C -->|Two| E[Result 2]
        ```
    ```

### Some Examples of Other Charts

#### Sequence Diagram

=== "Result"
    ```mermaid
    sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail!
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!
    ```

=== "Syntax"
    ```markdown
        ```mermaid
        sequenceDiagram
        participant Alice
        participant Bob
        Alice->>John: Hello John, how are you?
        loop Healthcheck
            John->>John: Fight against hypochondria
        end
        Note right of John: Rational thoughts <br/>prevail!
        John-->>Alice: Great!
        John->>Bob: How about you?
        Bob-->>John: Jolly good!
        ```
    ```

#### Gantt Chart

=== "Result"
    ```mermaid
    gantt
    dateFormat  YYYY-MM-DD
    title Adding GANTT diagram to mermaid
    excludes weekdays 2014-01-10

    section A section
    Completed task            :done,    des1, 2014-01-06,2014-01-08
    Active task               :active,  des2, 2014-01-09, 3d
    Future task               :         des3, after des2, 5d
    Future task2               :         des4, after des3, 5d
    ```

=== "Syntax"
    ```markdown
        ```mermaid
        gantt
        dateFormat  YYYY-MM-DD
        title Adding GANTT diagram to mermaid
        excludes weekdays 2014-01-10

        section A section
        Completed task            :done,    des1, 2014-01-06,2014-01-08
        Active task               :active,  des2, 2014-01-09, 3d
        Future task               :         des3, after des2, 5d
        Future task2               :         des4, after des3, 5d
        ```
    ```

#### Class Diagram

=== "Result"
    ```mermaid
    classDiagram
    Class01 <|-- AveryLongClass : Cool
    Class03 *-- Class04
    Class05 o-- Class06
    Class07 .. Class08
    Class09 --> C2 : Where am i?
    Class09 --* C3
    Class09 --|> Class07
    Class07 : equals()
    Class07 : Object[] elementData
    Class01 : size()
    Class01 : int chimp
    Class01 : int gorilla
    Class08 <--> C2: Cool label
    ```

=== "Syntax"
    ```markdown
        ```mermaid
        classDiagram
        Class01 <|-- AveryLongClass : Cool
        Class03 *-- Class04
        Class05 o-- Class06
        Class07 .. Class08
        Class09 --> C2 : Where am i?
        Class09 --* C3
        Class09 --|> Class07
        Class07 : equals()
        Class07 : Object[] elementData
        Class01 : size()
        Class01 : int chimp
        Class01 : int gorilla
        Class08 <--> C2: Cool label
        ```
    ```

