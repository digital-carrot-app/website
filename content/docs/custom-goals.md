---
title: Creating Goals
type: docs
weight: 10
# prev: /
# next: docs/folder/
---

There are three ways to create goals that vary by increasing complexity:

- Premade goals
- Custom goals
- Advanced editor

## Premade Goals

Premade goals don't require any programming knowledge whatsover. Simply pick one from the list and fill out the form:

{{< cards cols=2 >}}
  {{< card image="/images/docs/premade-goals.png" title="Available premade goals" >}}
  {{< card image="/images/docs/configure-premade.png" title="Configure a premade goal" >}}
{{< /cards >}}

These goals will handle everything for you from generating the goal to configuring the data needed for it.

## Custom Goals

The custom goal editor lets you build simple goals that can compare two values using a drag and drop editor.

{{< cards cols=2 >}}
  {{< card image="/images/docs/custom-goals.png" title="Create a custom goal" >}}
  {{< card image="/images/docs/configure-data-source.png" title="Configure a custom data source" >}}
{{< /cards >}}

This gives you much more fine grain control over your goals. For example, this allows you to create a goal based on your activities yesterday, which means that you will always be able to use whatever you blocked as long as past you is being a bro.

The app can infer a lot about your goals as long as they are set up. In this particular case it is able to tell that our goal is 400 calories and that I have currently burned 230.

![](/images/docs/custom-goal-progress.png)

## Advanced Editor

The advanced editor gives you direct access to the expression so that you can modify it however you want.

Goals are all evaluated using [expr expressions](https://expr-lang.org/). Expr is a super simple expression language that works a lot like spreadsheet functions. Expr expressions ingest any data that you decide to give it and resolve to a single value. In the case of Digital Carrot, they must resolve to either `true` or `false`.

This guide won't offer a comprehensive introduction to expr since the [expr website](https://expr-lang.org/docs/language-definition/) already does an excellent job of that.

All of your data is available to you in expr under the `data` variable. Variables can be dragged into the advanced editor in the same way as you would do with the basic editor.

![](/images/docs/drag-var.gif)

### Advanced Expressions with Expr

Lets say we want to hit a combination of steps plus exercise minutes for the day. We can write an expression like this:

```
let steps = data.movement_0.steps;
let exercise = data.movement_0.exercise_minutes;

let stepsPercent = (steps / 5000) * 100;
let exercisePercent = (exercise / 30) * 100;

exercisePercent + stepsPercent >= 100
```

This expression will track our step goal as well as our exercise goal. If the combined progress towards both of these goals goes above 100%, then the goal is completed. This means that you can make up for missing a few minutes of your workout by going on a walk!

The disadvantage of this expression is that it is too complicated for Digital Carrot to infer our progress:

![](/images/docs/advanced-goal-no-progress.png)

The program can only tell if the goal has been met, not how much progress we've made. To fix this, there are two custom functions in Digital Carrot:

- `progressText()`: this function takes in a string, or a template and a set of variables.
  - `progressText("You worked out for 30 minutes")`: this sets the progress text for your goal to "You worked out for 30 minutes".
  - `progressText("You worked out for %.0f minutes", data.movement_0.exercise_minutes)`: this dynamically inserts your variable into the progress message. The template string passed into the first argument behaves exactly the same way as `fmt.Sprintf` from Go. You can find the supported patterns on the [go documentation](https://pkg.go.dev/fmt). Some of the most common options are:
    - `%s`: insert a string
    - `%d`: insert an integer
    - `%f`: insert a floating point number
    - `%.2f`: insert a floating point number with 2 decimal places (ex: 10.00)
- `progressBadge(numerator, denominator)`: this function takes a numerator and a denominator. This will create a circular progress bar next to your goal.

Here is what this looks like in practice:

```
let steps = data.movement_0.steps;
let exercise = data.movement_0.exercise_minutes;

let stepsPercent = (steps / 5000) * 100;
let exercisePercent = (exercise / 30) * 100;

let total = exercisePercent + stepsPercent;

progressBadge(total, 100);

// Note that %% is the escape sequence for % in a formatted string.
progressText("Steps=%.0f%%, Exercise=%.0f%%, Total=%.0f%%", stepsPercent, exercisePercent, total);

total >= 100
```

This gives us a much prettier goal:

![](/images/docs/advanced-goal-progress.png)
