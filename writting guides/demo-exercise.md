---
layout: exercise

---


```md
:::walkthrough

All the content can be expressed in markdown

:::

:::exercise

::source['./path/to/exercise.{py|js|java}]
::solution['./path/to/solutuin.{py|js|java}]

:::
```
----

:::walkthrough

We can have separate exercises all contained and hence maintained within a single markdown file.

We can have as much written content placed here, this would then be places in the instructors panel.

```ts
const sample = "Some code sample"

function pattern (param:string):Void{
    return `The Sample says: ${sample}`
}

```
Can even place task lists here

[ ] - Have you done X?
[ ] - Have you done Y?

:::

:::exercise
::source['./path/to/exercise-file.ext']
::solution['./path/to/solution-file.ext']
:::

This would then allow us to populate the Interactive Learning Environment with the content needed to project each exercise to. 