<img src="/assets/images/paola-the-product-manager-slim.png" alt="Paola the Product Manager" style="width: 30%; float: right;" />

Product Managers drive and lead the team vision. They live at the
intersection of technology, user experience and the needs of the business by
staying connected to the needs of the the users and the problems that they have.

They clearly define the problem that the product is solving, and what outcomes
and goals need to be reached in order for it to be successful using
[User Stories][user-stories].

<img src="/assets/images/example-user-story.png" alt="Example user story" style="width: 30%; float: right;" />

Product managers work closely with [designers][designer] and
[software engineers][engineer] by defining [feature work][user-stories] and
prioritizing the order that features should be built in the
[backlog](./product-manager.html#backlog)


## Backlog

The __Backlog__ contains a list of features that Product Managers want Design and
Engineering to build for them. It includes a prioritized list of [User Stories][user-stories].

Below is an example of a __Backlog__ that is ordered from highest priority at the
top to the lowest priority at the bottom.

<img src="/assets/images/backlog.png" alt="The Product Backlog" />

Prioritizing the work in the __Backlog__ allows designers and engineers to work
together to start building the features.

<img src="/assets/images/kanban-board.png" alt="The Kanban Board" />

## User Stories

A user story is a way to describe a new feature that helps a user achieve a
specific goal. It describes a new feature that will to be built and
it also specifies [__criteria__](./product-manager.html#acceptance-criteria) that
must be met in order for the feature to be considered done.

The user story template:

> As a [role],
> I want to [do something]
> so that I can [achieve a goal].

A user story helps capture the user's voice and point of view by defining
__who__ will benefit from the feature, __what__ they want to accomplish and
__why__ they want to accomplish that.

### Examples

```plaintext
===============================================================================
  As a Teacher,
    I want to know when my students need help,
    so that I can provide them with the assistance that they need.
===============================================================================
  As a Student,
    I want to Sparkle one of my classmates,
    so that they can feel appreciated.
===============================================================================
```

<img src="/assets/images/user-stories.jpg" alt="Example user story" style="width: 30%; float: right;" />

## Acceptance Criteria

Product Managers define a list of things that must be completed in order for the
feature to be considered finished called __Acceptance Criteria__.
This list of items are added to the [__User Story__][user-stories] help Designers and Engineers
know if they have built a feature correctly.

### Examples

```plaintext
===============================================================================
User Story:

  As a Teacher,
    I want to know why my students need help,
    so that I can provide them with the assistance that they need.

  Acceptance Criteria:

  * [ ] The teacher must be notified when the student needs help.
  * [ ] The teacher must have a way to set up a 1:1 session with the student.
  * [ ] The student must provide a description of what they need help with.
...
===============================================================================
User Story:

  As a Student,
    I want to Sparkle one of my classmates,
    so that they can feel appreciated.

  Acceptance Criteria:

    * [ ] A sparkle must have a recipient.
    * [ ] A sparkle must have a reason.
    * [ ] The reason must be greater than 5 characters in length.
    * [ ] The reason must be less than 255 characters in length.
    * [ ] The recipient of the Sparkle must receive a notification.
...
===============================================================================
```

Next, learn more about the [Designers][designer] role.

[backlog]: ./product-manager.html#backlog
[criteria]: ./product-manager.html#acceptance-criteria
[designer]: ./designer.html
[engineer]: ./software-engineer.html
[issue]: https://github.com/CodeChica/SparkleHub-lite/issues/new
[user-stories]: ./product-manager.html#user-stories
