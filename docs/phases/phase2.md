# Phase 2: User Show Page, User Tasks Index, User Projects Index - Nav Bar

## Rails
### Models

### Controllers
Api::UsersController (show, tasks, teams, projects)

### Views
posts/feed.json.jbuilder
users/tasks.json.jbuilder
users/teams.json.jbuilder
users/projects.json.jbuilder

## Backbone
### Models

### Collections

### Views
* UserTasksIndex(composite view containing TaskIndexItem subviews)
* UserTeamsIndex(composite view containing TeamIndexItem subviews)
* UserProjectsIndex(composite view containing UserProjectIndexItem subviews)
* UserProjectIndexItem
* TeamIndexItem

## Gems/Libraries

