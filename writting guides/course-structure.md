# Course Structure

Courses can be thought of as a nested structure, where a course contains multiple chapters, each chapter contains multiple sections, and each section contains multiple components such as tutorials, units, and exercises. Let's explore how to best structure your files and folders to reflect this hierarchy.

## Organizing Files and Folders

Each course, chapter, section, and individual unit should be a separate Markdown file. These files should be organized in a hierarchical directory structure that mirrors the logical structure of your course. Here's a suggested approach:

```tree

course-name/
├─ README.md
├─ chapter-01/
│   ├─ README.md
│   ├─ section-01/
│   │   ├─ README.md
│   │   ├─ tutorial-01.md
│   │   ├─ unit-01.md
│   │   ├─ exercise-01.md
|   |   └─ exercises/
|   |       ├─ exercise-01.{js|ts|py|java}
|   |       └─ solution-01.{js|ts|py|java}
│   ├─ section-02/
│   │   ├─ README.md
│   │   ├─ tutorial-02.md
│   │   ├─ unit-02.md
│   │   └─ exercise-02.md
│   └─ ...
├─ chapter-02/
│   └─ ...
└─ ...

```

### In this structure:

The course-name directory is the root directory for the entire course. The `README.md` file in this directory serves as the main entry point of the course, containing the course's title, description, learning objectives, and an overview of the chapters.

Each `chapter-XX` directory corresponds to a chapter in the course. Similar to the course's `README.md`, each chapter's README.md provides an overview of the chapter and its sections (modules).

Each `section-XX` directory corresponds to a section or module within a chapter. Its `README.md` provides an overview of the section and its constituent parts: tutorials, units, and exercises.

The `tutorial-XX.md`, `unit-XX.md`, and `exercise-XX.md` files within a section directory correspond to the individual learning units within that section.

By keeping to a standard file naming nomenclature not only can we ensure that we are parsing the right files, but we can also establish that we are also navigating between the course content correctly.

## Breaking Down Chapters and Sections

To divide a chapter into sections and each section into its composing units (tutorials, units, exercises), consider the following:

### Outline your Chapter: 

Before you start writing, create an outline for your chapter within the chapter's `README.md`. This will give you a roadmap of what sections should be included, what each section should cover, and how they relate to each other.

A chapter is a major division in your course content. It often centers around a high-level theme or topic and includes several sections. 

#### Here are some tips for creating a good chapter:

Each chapter should have a clear goal or objective. What should the learner know or be able to do by the end of this chapter?

It should cover a significant concept or set of related concepts in the course material.
Use the chapter's README file to provide a brief overview of the chapter, its objectives, and the sections it includes.

### Create Sections: 

A section, or module, is a sub-part of a chapter. Each section should focus on a single topic or concept that contributes to the overall objective of the chapter. Think about logical groupings of content that will make the material easier to understand.

#### Here are some tips for creating sections:

Each section should cover a single, distinct topic or concept.

The objective of a section should be more specific than the objective of a chapter. What specific knowledge or skill should the learner gain from this section?

Use the section's README file to provide an overview of the section and its components: tutorials, units, and exercises.

### Create Tutorials, Units, and Exercises: 

For each section, identify what instructional materials (tutorials), topics for deeper study (units), and hands-on practice (exercises) you'll provide. These should be separate documents within the section directory.

### Tutorials

A tutorial is a learning unit designed to teach a specific skill or concept in a practical, step-by-step manner. 

Each tutorial should focus on teaching a single skill or concept.

Tutorials should be hands-on and practical. Whenever possible, show the concept in action. Using [`remark-directives`](./how-to/directives.md), you can express these concepts far better.

It's often helpful to start with an introduction to the concept, followed by the steps to use or implement it, and finally, an example or practice activity.

**Note**
> Remember, the key to a good structure is to make it logical and straightforward. The easier it is for students to navigate your content, the more effective their learning experience will be.


### Unit

A **unit** is a learning component that delves deeper into a specific topic. It's more theoretical compared to a tutorial and provides comprehensive knowledge on the subject. 

Units should cover the topic in depth and provide complete information. They are ideal for complex topics that need detailed explanations.

Theoretical explanations, examples, and references can be included in units.

Unlike tutorials, units do not necessarily have to be hands-on or practical, but they should clearly explain the concept or topic to the audience in a manner similar to use of the Feynman technique. Keeping it simple enough for others to easily understand it but not so simple that it dilutes the concept beyond the point of effective understanding.

### Exercise

An **exercise** is a specialized learning environment designed for hands-on practice. It allows learners to apply the knowledge they've gained from the tutorials and units. 

Each exercise should focus on a single skill or concept.

Exercises should be practical and hands-on. They should provide a problem or task for learners to solve or complete.

Providing solutions (either immediately after the exercise or at the end of the section) can be beneficial for learners to check their work and understanding.

Exercises should encourage active learning. They should be challenging but achievable, promoting critical thinking and problem-solving.


We will in due course be breaking these individual concepts: "Course, Sections, Tutorials, Units and Exercises" into further detail as we fully develope this process. Taking on best practices and learned experiences from content authors to help design and provide insight and context to these concepts. 