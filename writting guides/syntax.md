
# Syntax

We will be extending the syntax of our markdown language to help provide better semantic value for the content we are wishing to express.

All our syntax that we will be using is an extension upon the existing standard Markdown syntax. This would allow you to write existing markdown syntax without a break in expectation.

We are incorporating two additional syntax styles to help augment our markdown experience with `github-flavored-markdown` (`gfm`) and `remark-directives`. 

## Basic Markdown Syntax

The basic syntax of Markdown includes elements like headings, paragraphs, bold and italic text, links, lists, images, blockquotes, inline code, and code blocks.

- **Headings**: 
    Use `#` for a level-one heading, `##` for a level-two heading, and so forth, up to six levels.
    ```md
    # Heading 1
    ## Heading 2
    ### Heading 3
    #### Heading 4
    ##### Heading 5
    ###### Heading 6
    ```

- **Paragraphs**: 
    Separate paragraphs by a blank line.

- **Bold text**: 
    Use `**` surrounding the text you wish to mark as bold.
    ```md
    **text**
    ```

- **Italic text**: 
    Use `*text*` to mark text as being emphasized.
    ```md
    *empashised text*
    ```

- **Links**: 
    Use `[text](URL)`. When linking across files using titles use `[text](#title)` to create a hash link to the title. When linking between pages, make sure you have taken into consideration the location of the current file relative to the file you are linking to. Also remove the file extension of the file that you are linking to if it happens to be another markdown file, as the links do not get parsed during post-processing.

- **Lists**: 
    Use `-` for bullet lists, or `1.` for numbered lists. There is no hard rule with a new line before or after the use of a new list item. It is preferential, however it does make it easier to manually parse if there is appropriate spacing applied around list items. 

- **Images**: 
    Use `![alt text](URL)`. All Images must have a **alt** text filled in. Relative links must ensure they are based off the location of the markdown file. Where at all possible use Absolute URL references for image paths. Since your content maybe processed elsewhere it makes it significantly easier to display images as expected if they are already hosted on a online provider via a CDN.

- **Blockquotes**: 
    Use `>` to display quoted statements.
    ```md
    > There was once a fuzzy bear
    ```
    This gets rendered as:
    > There was once a fuzzy bear

- **Inline code**: 
    Use single back-ticks `` `code` `` to create inline codeblocks, these are not highlighted by syntax highlighting support.
    ```md
       This is some `code` in a sentence. 
    ```
    This renders out as:

    This is some `code` in a sentence.

- **Code blocks**: 
    Use triple back-ticks ` ``` ` around a block of code. You can specify the language of the code in the following way ` ```lang `. This would instruct the correct use of syntax highlighting to take effect on the code block. This also ensures it gets rendered out to `html` correctly.

    <!-- TODO: This needs to be a more expansive Guide on Basic Syntax -->

## Github Flavored Markdown (`gfm`)

GFM adds some additional features to standard Markdown:

- Task Lists: 
    You can create task lists using - `[ ]` for an uncompleted task and - `[x]` for a completed task. For more information see our [guide on Task Lists](./guides/task-list)
- Tables: 
    You can create tables by assembling a list of words and dividing them with hyphens `-` (for the first row), and separating each column with a pipe `|`.
     For more information see our [guide on using Tables in Markdown](./guides/tables)

- Autolinked References: 
    GFM will automatically link references to commits, pull requests, issues, and users directly to the relevant sections on GitHub.
    For more information see our [guide on Autolinked References](./guides/gfm)

## Remark-Directives

Remark-Directives allows you to add custom syntax to your Markdown files. The basic syntax is:

```md
::name[contents]
```

Here, name is the name of the directive, and contents is the contents of the directive. The contents can be omitted if not needed.

It follows the following syntax patterns.

```md
::myDirective{html attributes} [content]
```

There are three types of directives: 
- leaf (`::`), 
- container (`:::`) requires a closing `:::` 
- and text directives (`:`). 

Leaf and container directives can have attributes. However Text directives can have attributes added after the `[content]` field.

Attributes obeys the following pattern:

```md
{#id .class key=value}
```

We would be developing custom components that would be used by content authors within their content via the use of directives. This allows us to provide those rich content experiences without sacrificing content authoring experience within Markdown.

For further information on how to use `remark-directives` [read our guide](./guides/directives).