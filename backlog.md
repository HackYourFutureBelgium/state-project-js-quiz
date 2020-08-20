# Backlog

A collection of user stories you can choose from.  Stories inside of each priority level are not necessarily in order, it's up to your group to decide how they fit into your strategy.  These are also just suggestion, feel free to change them or create your own!

## Must-Haves

> these are necessary for basic usability

- [ ] A user can see all questions at once
- [ ] A user can select an answer for each question
- [ ] A user can know which questions they got correct and incorrect
- [ ] A user can see the correct answer for questions
- [ ] A user can see their score at the end of the quiz

## Should-Haves

> these will complete the user experience, but are not necessary

- [ ] A user can see one question at a time, stepping through the quiz (may require refactoring)
- [ ] A user can "cheat" to see the correct answer, this forfeits the question
- [ ] A user has access to resources for further study on each question
- [ ] A user can see their score update in real-time as they select answers

## Could-Haves

> would be really cool ... if there's time

- [ ] A user can modify a question in the quiz
- [ ] A user can remove questions from the quiz
- [ ] A user can add questions to the quiz

---
---

# From Backlog to Strategy

1. [Prioritizing](#prioritizing)
2. [Acceptance Criteria](#acceptance-criteria)
3. [Defining Tasks](#defining-tasks)
4. [Project Board](#project-board)
5. [Sprinting and Reviewing](#sprinting-and-reviewing)

## Prioritizing

How to decide which stories to develope first.

- [Alex Ponomarev](https://medium.com/swlh/prioritizing-user-stories-in-agile-projects-d1dd8dd79165)
- [Michael Lant](https://michaellant.com/2010/05/21/how-to-easily-prioritize-your-agile-stories/)

## Acceptance Criteria

How you'll know when the story is finished.

- [Yodiz](https://www.yodiz.com/blog/user-stories-acceptance-definition-and-criteria-in-agile-methodologies/)
- [Zepel](https://zepel.io/agile/acceptance-criteria-for-user-stories/)
- [Ruby Garage](https://rubygarage.org/blog/clear-acceptance-criteria-and-why-its-important)
- [The Infinity Project](https://www.youtube.com/watch?v=KYS0ptJ4JWc) +1
    1. User Input / User Action
    2. Process
    3. Results

## Defining Tasks

How to break the story into coding tasks. (`development-strategy.md`)

Answering these questions is a way to break down complex user stories and to determine what code is needed:

1. **User Story Objectives**
    1. _What should change in state after this user story is complete?_
    2. _How will the UI represent these state changes for the user?_
2. **Gathering Data**
    - What data do we need from state?
        1. _Is it already available in state?_
        2. _Can I compute it from existing state data?_
        3. _Do I need to hard-code it into state?_
    - What data do we need from the user?
        1. _What action does the user take? (click, hover, type, ...)_
        2. _Should the user interact with an existing ui element?_
        3. _Do I need to add elements to the UI?_
        4. _How do I collect data I need? (`event`, DOM access, ...)_
        5. _How do I check or clean the user input?_
3. **Core Logic -> combine/transform gathered data**
    1. _Do I need different behaviors for different states?_
    2. _Do I need different behaviors for different user inputs?_
    3. _What new data do I expect after this story is finished? (see objectives)_
    4. _Can this data be generated simply inside the handler?_
    5. _Can I reuse logic from another user story?_
    6. _Do I need to write a new logic function for this story?_
4. **Register Changes**
    - Add the new data to state (see _objectives_)
        1. _Do I need to remove any data from state?_
        2. _Should this replace data that is currently in state?_
        3. _Should it be added as a new field in state?_
    - Update the UI to reflect the new state (see _objectives_)
        1. _Does the UI need to be updated?_
        2. _Can it happen in the handler with simple dom manipulation?_
        3. _Can I reuse a view function from another story?_
        4. _Do I need to write a new view function?_

handlers are the glue of your user stories.  understanding your answers to these questions will guide the development of your handlers and will help you decide what other tasks to create.

- [Lars Bilde](https://www.youtube.com/watch?v=gZ4uLafsxAk)
- [Christiaan Verwijs](https://medium.com/the-liberators/10-powerful-strategies-for-breaking-down-user-stories-in-scrum-with-cheatsheet-2cd9aae7d0eb)

> PS. logging is a [_cross-cutting concern_](https://en.wikipedia.org/wiki/Cross-cutting_concern). it does not have a separate step because it should be incorporated into each step of your handler

## Project Board

Convert your development strategy into milestones (user stories), issues, labels and a project board.

This isn't a permanent thing! You can always adjust the project board and development strategy as the project evolves; adding issues, removing issues, adjusting tasks ... whatever is necessary to make the project go smoothly.

## Sprinting and Reviewing

The fun part, writing code and closing issues ;)
