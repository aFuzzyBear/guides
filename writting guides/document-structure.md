---
title: Document Structure
author: Fuzzy
description: Breaking up the document in the best possible way
draft: true

section: guides
sub: writing
unit: document structure
---
# Document Structure

The mantra, "There are many ways to write markdown," intimates that there are also many ways to structure content. 

Without function, there is no formal shape or appearance to something, and without structure, there is no definition for the function.

This guide sets out ways to make it easier for content creators to bring both form and structure to their writing style. This allows them to express their content more freely, knowing that they are executing their function with purpose. 

## Structuring a Single Document

It all starts from the top. Adopting certain rules and styles can provide a unified structure to each type of document we create.

There are different types of documents or single units of content, each resulting in a different visual presentation of the authored content. The type of the document: "Tutorial," "Unit," or "Exercise" can be stored on each page, along with other types of metadata.

Structuring a single document in a clear, logical, and digestible way is crucial for effectively communicating your content. Here's some guidance on how to do this:


### Title

The title should be clear and concise, indicating the main topic or purpose of the document. Use Markdown's `#` syntax for the title. This also helps with creating a table of contents.

For further guidance on how to write clear and meaningful titles [read here](./semantics.md/#1-use-clear-specific-and-meaningful-titles-and-subheadings)

```md
# Title of the Document
```

### Introduction or Overview

Start with an introduction that provides an overview of what the document will cover. This helps set the readers expectations.

```md
## Introduction

In this document, we will explore...
```

### Main Content

Divide the main content into logical sections and subsections using Markdown's heading syntax (`##`, `###`, etc.). This not only makes the document more readable but also automatically creates a navigable table of contents on platforms like GitHub.

Each section should have a clear focus and should ideally be self-contained, meaning a reader can understand the content of that section without needing to refer back to earlier content.

```md
## Main Section 1

Content of the main section 1...

### Subsection 1

Content of the subsection 1...
```

Use Markdown formatting such as bold (`**bold text**`), italics (`*italicized text*`), and lists (`- item`) to make the content easier to read and understand.

### Code Blocks

If your document includes code, use Markdown's syntax for code blocks. This makes the code stand out from the regular text and preserves its formatting. You can also specify the programming language for syntax highlighting.

    ```javascript
    function helloWorld() {
        console.log("Hello, world!");
    }
    ```

### Images and Diagrams

Images and diagrams can be inserted using Markdown's syntax and can greatly enhance the clarity of your content. Be sure to include alt text for accessibility.

```md
![Alt text for image](url-to-image)
```

### Links

Links to external resources can be included using Markdown's syntax. This is especially useful for providing additional reading or for citing your sources.

```md
For more information, see [this link](url-to-link).
```

### Thematic Breaks

Thematic breaks (`***`) are used to create a horizontal line in your document, providing a clear visual separation between different sections or ideas. They can be particularly useful to break up long documents or to mark transitions between different topics or themes.

When you want to add a thematic break to your document, you should insert a line with three asterisks on a new line, like this:

```md
***
```

Here are some guidelines for using thematic breaks:

**Consistency:** 
To keep your documents looking uniform, try to use thematic breaks consistently. For example, you might choose to always place a thematic break before a new section begins.

**Whitespace:** 
Make sure to put an empty line before and after your thematic break. This will ensure that it stands out and is not mistaken for an underline.

**Don't overuse**: 
While thematic breaks can be very helpful, they should not be overused. Too many breaks can make a document look disjointed and can disrupt the flow of the text. A good rule of thumb is to use them sparingly and only where there is a clear change in topic or theme.

#### Example
Here is an example of how a thematic break can be used:

```md
## Section 1

This is some text about a particular topic. 

***

## Section 2

This is some text about a different topic.
In this example, the thematic break between the sections helps to clearly delineate where one topic ends and the next begins.
```


### Conclusion or Summary

End the document with a conclusion or summary that recaps the main points. This helps to reinforce what the reader has learned.

```md
## Conclusion

In this document, we have covered...
```

### Frontmatter / Metadata

Don't forget to include metadata in the frontmatter (`---` fence block) to the top of your document. This would typically include information like the document's author, date, and keywords, and it can also include more specific data like the chapter, section, and module numbers.

```md
---
title: "Title of the Document"
author: "Author's Name"
date: "YYYY-MM-DD"
chapter: 1
section: 2
unit: 3
keywords: "keyword1, keyword2"

---
```

### Defining Layouts

We can use frontmatter to help define additional metadata about the document. With this we can at build-time (that is when we process the markdown onto our frontend), use this metadata to add further *'directives'* to the User Interface (UI).

For instance when we are creating our content we have several different formats that we would be creating. "Overview" or "README" pages would be parsed and displayed differently to a "Unit" and likewise there would be implementation differences between a "Tutorial" and an "Exercise".

However, from the content authoring experience we do not wish for this to distract the content creators from their creation's process. If anything they only stipulate which type of document they are working on. With this knowledge imparted, matching the layouts to the correct document type would be done automatically during build-time.

```diff
---
title: "Title of the Document"
+ doctype: "overview" | "unit" | "tutorial" | "exercise"
author: "Author's Name"
date: "YYYY-MM-DD"
chapter: 1
section: 2
unit: 3
keywords: "keyword1, keyword2"

---

```
For reference here are the accepted `types` for `doctype`:

```ts
// Doctype for reference
type doctype = "overview" | "unit" | "tutorial" | "exercise"
```
***

By structuring each document in this way, you'll ensure that the content being created is well-organized and easy to follow.