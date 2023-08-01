---
title: How to use Task Lists in Markdown
author: fuzzy
draft: true
description: A short guide on how to use Task Lists in Markdown

section: guides
    sub: how to's
    unit: task list
---
# Using Task Lists in Markdown

Task lists are lists with items marked as either done or not done. They are useful for tracking progress on a set of tasks.

## Creating Task Lists

To create a task list:

1. Start with a normal unordered list by typing a hyphen `-` or an asterisk `*`.

2. Follow the hyphen or asterisk with a pair of square brackets `[]`. 

3. If the task is complete, you add an `x` between the square brackets `[x]`. If the task is not complete, leave the square brackets empty `[]`.

Here's an example:

```markdown
- [x] Complete task 1
- [ ] Complete task 2
- [ ] Complete task 3
```

This will create a task list that looks like this:

- [x] Complete task 1
- [ ] Complete task 2
- [ ] Complete task 3

## Do's and Don'ts

- Do use task lists to track progress on a set of tasks.
- Do use an `x` to mark tasks as complete.
- Do remember that task list items are case-insensitive; `[x]` and `[X]` are equivalent.
- Don't use other characters besides `x` or `X` between the brackets to mark tasks as complete; they won't render as a checked box.
- Don't forget the space after the hyphen or asterisk; without it, the task list won't render correctly.


Remember that while task lists are a great way to track progress, they don't offer functionality beyond marking items as done or not done. For more complex use-cases or requirements please use a [remark-directive](./directives). 
