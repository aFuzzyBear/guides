---
title: How to use Tables in Markdown
author: Fuzzy
draft: true

description: A short guide on how to use Tables in Markdown.

section: guides
    sub: how to's
    unit: tables

---
# Using Tables in Markdown

Markdown allows you to create tables using pipes `|` and hyphens `-`. Below is a guide on how to create and format tables.

## Creating Tables

To create a table:

1. Write the column headers, separated by pipes (`|`).

2. Create a separating line using hyphens (`-`). This line separates the table headers from the table rows.

3. Write the table rows, with each cell separated by a pipe (`|`).

Here's a simple example:

```markdown
| Header 1 | Header 2 |
|----------|----------|
| Cell 1   | Cell 2   |
| Cell 3   | Cell 4   |
```

This will create a table like this:

| Header 1 | Header 2 |
|----------|----------|
| Cell 1   | Cell 2   |
| Cell 3   | Cell 4   |

## Aligning Text

You can align text in the columns to the left, right, or center by including colons `:` in the line below the header:

- Left-aligned: `:-----`
- Right-aligned: `-----:`
- Center-aligned: `:-----:`

Example:

```markdown
| Left-aligned | Center-aligned | Right-aligned |
|:-------------|:--------------:|--------------:|
| Cell 1       | Cell 2         | Cell 3        |
| Cell 4       | Cell 5         | Cell 6        |
```

This will render as:

| Left-aligned | Center-aligned | Right-aligned |
|:-------------|:--------------:|--------------:|
| Cell 1       | Cell 2         | Cell 3        |
| Cell 4       | Cell 5         | Cell 6        |

## Do's and Don'ts

- Do remember to keep the number of hyphens and pipes consistent across all rows. This ensures that the table renders correctly.
- Do align the text in your table cells for better readability.
- Don't forget to separate your headers from your cells with a line of hyphens and pipes.
- Don't include pipes or backslashes in your cell content without escaping them first. Use `\|` or `\\` to include these characters in your cell content.
- Don't leave out the separating line below the header; it's necessary to render the table correctly.


Remember that while Markdown tables are a great way to present data, they are limited in terms of formatting and functionality compared to something like a customized HTML table web component.
