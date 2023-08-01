---
title: Guide on How to Use Autolinked References in GitHub Flavored Markdown
author: Fuzzy
draft: true
description: A short guide on how to use Autolinked References in Github Flavored Markdown.

section: guides
    sub: how to's
    unit: gfm
---

# Guide on How to Use Autolinked References in GitHub Flavored Markdown (GFM)

Autolinked References is a feature in GFM that automatically turns certain text patterns into links to the corresponding entities on GitHub. It can link to user profiles, issues, pull requests, and commit hashes.

## How to use Autolinked References

### Linking to Users

To create a link to a user's profile, simply type @ followed by the user's username. GFM will automatically turn it into a link to the user's GitHub profile.

Example:
```md
Thanks for the contribution, @octocat!
```

The above example will render as: 
`"Thanks for the contribution, @octocat!"`

### Linking to Issues and Pull Requests

You can reference an issue or a pull request in your content by typing # followed by the issue or pull request number. GFM will turn this into a link to the specific issue or pull request in the current repository.

Example:

```md
This bug was fixed in #42
```

The above example will link to the issue or pull request number 42 of the **current repository**.

### Linking to Commits

Referencing a commit is just as simple. Include the SHA hash of a commit in your content and it will automatically become a link to that commit.

Example:
```md
This was fixed in commit a5c3785ed8d6a35868bc169f07e40e889087fd2e
```
The above example will create a link to the commit with the hash `a5c3785ed8d6a35868bc169f07e40e889087fd2e`.

Linking to Items in a Different Repository

If you want to link to issues, pull requests, or commits in a different repository, you'll need to use the full GitHub path: username/repository#issue.

Example:
```md
Refer to the issue octocat/Hello-World#42 for more details.
```
The above example will link to issue number 42 in the "Hello-World" repository owned by "octocat".

## Dos and Don'ts

- Do use Autolinked References to simplify navigation and cross-referencing in your GitHub projects.

- Do remember to include the full GitHub path when referencing entities in a different repository.

- Don't rely on Autolinked References for linking to external resources. It only works for internal GitHub entities.

- Don't include additional formatting (like bold or italic) within your Autolinked References, as it may prevent them from being correctly parsed and linked.