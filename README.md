# Nexproc

## Minimum Viable Product
Nexproc is a clone of Asana that is  built on Rails and Backbone. Users can:

<!-- This is a Markdown checklist. Use it to keep track of your progress! -->

- [X] Create accounts
- [X] Create sessions (log in)
- [X] Create teams
- [X] Create projects
- [X] Create tasks
- [X] Add members to team
- [ ] Comment on Tasks
- [X] Fall in Love with their Swanky Side-Nav Bar
- [X] Navigate to Teams
- [X] Navigate to Projects
- [X] Navigate to Tasks

## Design Docs
* [View Wireframes][views]
* [DB schema][schema]

[views]: ./wireframes.pdf
[schema]: ./docs/schema.md

## Implementation Timeline

### Phase 1: User Authentication and Team, Project, Task, and Comment creation. (~1 day)
I will do most of the backend, Rails setup for the primary features of my project. Afterwards, I'll be aiming to get my project up and running on Heroku.

[Details][phase-one]

### Phase 2: User Show Page, User Tasks Index, User Projects Index + Navigation Bar (~1-2 days)

The navigation bar will have links to the Teams, Projects, and Tasks indices for the current user.

Using the data nested within User > Teams > Projects, I will create a UserProjectIndex that will show all of the projects that the user is currently a part of, the name of the team that is overseeing it, and the completed number of tasks next to the total number of tasks.
The Second feature added in this phase will be an Index of any task that has been directly assigned to the current user.

[Details][phase-two]

### Phase 3: Viewing your teams, their team Members, and projects (~2 days)
In this phase, I will use JSON to parse a team's nested collection of both, team members and that team's projects. This will be contained within a TeamShow view.

[Details][phase-three]

### Phase 4: Viewing a Project's Tasks, implementing TaskShow (~2 days)
This phase will involve creating the show pages for the Projects themselves. The project's show page will consist of a tasks index. These tasks will need to be parsed using JSON builder. The tasks themselves will need their own show pages and should be able to contain an index of their own sub-tasks - I will try to accomplish this using the same nested comments pattern that we used on the Reddit Clone.

[Details][phase-four]

### Phase 5: Add Comments index/form to the Tasks list (~1 day)
A comments index view will be added to the Tasks view, below the subtasks.

[Details][phase-five]

### Bonus Features (TBD)
- [ ] Cool, slidey CSS.
- [ ] Built-in team-chat
- [ ] RSS Task Activites (user edits task, etc.)
- [ ] Project/Task/Team searching
- [ ] Typeahead search bar
- [ ] Multiple sessions/session management

[phase-one]: ./docs/phases/phase1.md
[phase-two]: ./docs/phases/phase2.md
[phase-three]: ./docs/phases/phase3.md
[phase-four]: ./docs/phases/phase4.md
[phase-five]: ./docs/phases/phase5.md
