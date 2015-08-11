# Phase 2: Viewing Blogs and Posts

## Rails
### Models

### Controllers
Api::TeamsController (create, destroy, index, show)
Api::ProjectsController (create, destroy, show, update)

### Views
* teams/show.json.jbuilder

## Backbone
### Models
* Team (parses nested 'projects' and 'team members' associations)
* Project

### Collections
* Teams
* Projects

### Views
* TeamForm
* TeamShow (composite view, contains TeamProjectsIndex subview)
* TeamProjectsIndex (composite view, contains TeamProjectsIndexItem subviews)
* TeamProjectsIndexItem (composite view, contains TeamMemberIndexViews)
* TeamMemberIndexView
* ProjectsIndex (composite view, contains ProjectsIndexItem subviews)
* ProjectsIndexItem

## Gems/Libraries
