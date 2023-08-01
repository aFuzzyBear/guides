---
title: Using `remark-directives` in Markdown
author: Fuzzy
draft: true

description: A short guide on how to use directives withing your Markdown directly.

section: guides
    sub: how to's
    unit: remark directives
---
# Using `remark-directives` in Markdown

`remark-directives` is a powerful tool that enables the usage of custom syntax in Markdown files. This guide explains the syntax, rules, and provides examples for the various directive types: leaf, container, and text.

## Syntax and Rules

There are three types of directives: 

1. **Leaf directives**: Standalone elements denoted by double colons `::`.

```markdown
::myDirective{#id .class key=value}
```

2. **Container directives**: Elements which contain other elements. They begin with triple colons `:::` and close with the same.

```markdown
:::myDirective{#id .class key=value}
contents
:::
```

3. **Text directives**: Elements within a text node.

```markdown
This is a :myDirective[contents]{#id .class key=value}.
```

The `{#id .class key=value}` part is optional and used to specify an `id`, a `class`, or other attributes for the directive. This can be placed before the content as with leaf and container directives, or at the end as demonstrated with the text directive.


## Rules

- Directive names must consist of alphanumeric characters and can include dashes, underscores, and periods.
- Directive names are case-sensitive.
- IDs should be unique within a document.
- Classes can be reused across directives in a document.
- HTML attributes follow the pattern `key=value`.

## Examples

```markdown
// Leaf directive with class 'yellow'
::highlight{.yellow}[This is content that would need to be highlighted] 

// Container directive with ID 'tip' and class 'boxed'
:::info{#tip .boxed}
This is a helpful tip.
::: 

// Text directive with content 'Remember this!' and ID 'note1'
This is a :note[Remember this!]{#note1} within a text block
```

## Do's and Don'ts

- **Do** ensure that your directive names are alphanumeric and contain no spaces.
- **Do** ensure IDs are unique within a document.
- **Do** use HTML attributes to enhance the styling and functionality of directives.
- **Do** use classes for applying shared styles across multiple directives.
- **Don't** put a space between the colons `::` or `:::` and the directive name.
- **Don't** forget to match your opening and closing colons `::` or `:::` for leaf and container directives, respectively.
- **Don't** use made up directives. Only use known directives as they correspond to their companion web components. Not all directives are instantly provided, if you have a request for one please raise it as a [github issue]()
<!-- TODO: Find a place to raise specific issues to github -->

There would be a separate directives list that would contain all the registered directives and their associated documentation on usage within the scope of the content team.

Please remember that the actual processing and rendering of directives will depend on the configuration of our Markdown processor. 

This guide should provide a comprehensive overview of using `remark-directives`. The rules described can also be used to instruct linters to check the proper usage of `remark-directives`.


While it is technically feasible to use the same directive in all three forms of directive types, it's essential to carefully consider design implications. Each directive corresponds to an HTML web component, which can be utilized post-processing. During the content authoring phase, we simply place markers where we want the directives to appear within the document, along with any additional data that the directive should contain.

However, this approach means that the development of such components could be quite brittle, as they would need to accommodate three different types of directive implementations. For instance, using Container Directives would require the component to handle `slot` behavior, a consideration that isn't necessary with the other two types. 

```md
This is a small example of how to add and annotate Quiz's within your document

<!-- We need a quiz id and a title for the quiz component -->
:::Quiz{quiz-id=1.1 title="Color of the Sky"}

<!-- Content placed in here would be slotted into the component -->
::Question [What is the color of the sky]

<!-- We can also have nested leaf directives if they are designed to do so -->
::choice [ Green ::explanation [ If we had alot of methane instead of nitrogen in the sky, then this might be possible, then again life wouldn't ] ]

::choice{correct=true} [Blue]

<!-- Closing tag for the Container directive -->
:::

```

```js

```

For those interested in developing their own remark directives and components, we'll soon follow up with a comprehensive guide on how to do so.

