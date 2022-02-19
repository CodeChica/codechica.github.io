# Final Project

In teams of 3 people, you will create 1 new feature for [SparkleHub][sparklehub].
Each team will choose who will be the [Product Manager][product-manager],
[Designer][designer], and [Engineer][engineer].

* The Product Manager creates a [User Story][user-story] submitted as a [new issue][issue].
* The Designer creates a [Wireframe][wireframe] of the feature submitted as an attachment in the issue.
* The Engineer creates a [Task breakdown][tasks] of the work to be done to build the feature included in the issue.
* The team submits a [Pull Request][pull-request] to the [SparkleHub][sparklehub] repo with working code.

Each member of the team will present how they contributed to the feature that they worked on together.

## Example

```plaintext
User Story:

As a Sparkler,
I want it to rain confetti when I send a Sparkle,
so that I know that my Sparkle has been sent.

Acceptance Criteria:

* Rainbow coloured confetti will rain down when a new Sparkle is created.
* The confetti will stop raining when it reaches the bottom of the screen.
* The text "You sent a Sparkle!" will appear behind the confetti.

Wireframe:

  -------------------------------
  | o  @  o     o @ @ o @ o  0  |
  |   @ o    o @  @ o   o  o  o |
  |  o   @ o   @@ o   o  @ o o  |
  |      o                o     |
  |   o               o         |
  |                             |
  |     🎉 SPARKLE SENT  🎉     |
  |                             |
  |                             |
  |    /\/\      \🥳            |
  | /\/  \ \/\    ||\           |
  |/      \   \   /\            |
  -------------------------------
  |         SparkleHub          |
  -------------------------------

Tasks:

* [ ] Research how to create a confetti animation. (large)
* [ ] Build a prototype of the confetti animation. (large)
* [ ] Share a demo of the prototype and collect feedback. (medium)
* [ ] Trigger the confetti animation after the Sparkle is saved. (small)
* [ ] Stop the animation after `n` seconds using a timer. (small)
* [ ] Measure the memory usage in the browser. (medium)
* [ ] Add automated tests for each of the browsers that we support. (medium)
* [ ] Work with Design to choose colours that are accessible. (small)
* [ ] Add acceptance tests for the new animation. (medium)
```

[designer]: /plus-plus/roles/designer.html
[engineer]: /plus-plus/roles/software-engineer.html
[issue]: https://github.com/CodeChica/SparkleHub-lite/issues/new
[product-manager]: /plus-plus/roles/product-manager.html
[pull-request]: https://github.com/CodeChica/SparkleHub-lite/compare
[sparklehub]: https://github.com/CodeChica/SparkleHub-lite
[tasks]: /plus-plus/roles/software-engineer.html#task-breakdown
[user-story]: /plus-plus/roles/product-manager.html#user-stories
[wireframe]: /plus-plus/roles/designer.html#what-is-a-wireframe
