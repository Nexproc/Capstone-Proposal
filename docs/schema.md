# Schema Information

## users
column name     | data type | details
----------------|-----------|-----------------------
id              | integer   | not null, primary key
username        | string    | not null, unique
password_digest | string    | not null
session_token   | string    | not null, unique
profile_picture | blob      |

## projects
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
title       | string    | not null
team_id     | integer   | not null, foreign key (references teams)
description | text      |

## teams
column name    | data type | details
---------------|-----------|-----------------------
id             | integer   | not null, primary key
owner_id       | integer   | not null, foreign key (references users)
name           | string    | not null

## team_members
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
team_id     | integer   | not null, foreign key (references teams)
member_id   | integer   | not null, foreign key (references users)

## tasks
column name    | data type | details
---------------|-----------|-----------------------
id             | integer   | not null, primary key
project_id     | integer   | not null, foreign key (references projects)
parent_task_id | integer   | foreign key (references tasks)
assigned_to    | integer   | foreign key (references users)
body           | text      |
completed      | boolean   | not null, default = false
due_date       | date      |
begin_date     | date      |

##comments
column name    | data type | details
---------------|-----------|-----------------------
id             | integer   | not null, primary key
task_id        | integer   | foreign key (references tasks)
author_id      | integer   | not null, foreign key (references users)
title          | string    | not null
body           | text      |

####Extras

## tags
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
label       | string    | not null, unique

## taggings
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
task_id     | integer   | not null, foreign key (references projects)
tag_id      | integer   | not null, foreign key (references tags)

##task_activities
column name | data type | details
------------|-----------|-----------------------
id          | integer   | not null, primary key
user_id     | integer   | not null, foreign key (references projects)
task_id     | integer   | not null, foreign key (references tags)
action_type | string    | not null

### other activities will be a collection of activities linked to child-tasks
### team member roles and actions