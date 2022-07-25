# Table of Contents

## Legacy Code Projects

* Choosing Legacy Code Projects (what do we look for?)
* Tech Stack (current, how it has evolved, why)
* Application Lifecycle
  * Development, QA, Production
* How do we set it up? (demo-spring-react-example)
  * Staff setup before handoff to students
  * Branch protection rules
* How do we migrate from one quarter to another?
* How do we come up with issues and epics?
* How do we make use of starter stories?
* How do we introduce legacy code projects to the students?
* What do we look for in pull requests for the legacy code projects?
  * Two reviews, one from another team member, one from staff
  * Detailed description with linked issue
* Grading, Point System
  * Get to 100, points are 5, 10, or 20, depending on complexity of work
* Common Pitfalls for students when approaching Legacy Code
  * Smaller, incremental PRs instead of one giant PR
  * Doing the wrong thing well - predictable outcomes
    * Students often write very good code but have a flawed understanding of what the issue at hand is actually for, so they write code that has to be thrown away

## Services

* GitHub
  * Organizations, Teams, and Initial Setup
  * Student Developer Pack (and Teacher Pack)
  * Legacy Code Project Repositories
  * Issues and Projects (Kanban Boards)
    * Talk about Projects Beta, how it could be incorporated?
  * Pull Requests
  * Actions / Secrets
  * Pages (static website hosting)
* UCSB CS GitHub Linker (Anacapa)
  * Initial Setup
  * Team Importing (and what it affects)
  * Analysis Tools
  * Creating empty repositories for assignments
* Heroku
  * Two-factor authentication
  * Setup of Heroku apps for CS 156 (production, QA)
  * Limitations of Heroku (credit cards, being on top of grading)
  * Postgres
* Slack
  * Initial Setup
  * Channel Layout (and each channel's purpose)
  * #help-lecture-discussion
  * Anacapa Slack Bot
* Gradescope and Gauchospace
  * Initial Setup (production and staff instances)
  * Initial Student Emails
  * Team Imports
  * Assignment Templates
* Testing
  * Unit Testing: JUnit and Jest
  * Mutation Testing: Pitest and Stryker
  * Codecov
    * Integration with GitHub, reports / checks that show up on pull requests
    * CODECOV_TOKEN, when you need it, how to set it up
    * Approving students
    * Common gotchas when setting up / using Codecov
      * Make sure the branch name is correct (main vs. master)
  * GitHub Actions (just link to above?)
* Development Tools
  * VS Code
  * Swagger UI
  * Storybook
    * GitHub Pages deployments for QA and Prod
    * DOCS_TOKEN, how to set it up
  * MongoDB
    * How it's currently being used, why choosing this over Postgres
    * Setting up a new MongoDB org for a class iteration
      * Invite first, student accepts, then introduce to team
  * UCSB Developer API
    * Where it's used in our apps
    * Requesting an account, sharing keys

## Teams and Team Formation (CATME)

* Initial Survey for team formation
* Section swaps
  * How to handle them
  * Procedure for students to request them
* Periodic CATME Evaluation Surveys
  * Why do we do them?
  * How do they factor into a student's grade?
* Importing teams into GauchoSpace, GitHub Linker

## The Course Website

* Organization and Layout
  * Topics and Resource section
  * Labs, lectures, and homework list
  * Office Hours and Calendar
  * Team Member List
  * How to create / update all of the above
* Software installation article
* Creating a New Quarter on the website

## Agile Workflows

* General overview of Agile concepts, description of which concepts we implement as-is, description of concepts we modify to work in a short academic setting
* Standups
  * How and when do we introduce?
  * How do we do them? (Posting on Slack for participation)
* Retrospectives
  * How and when do we introduce?
  * How often do we do them? (After every team assignment)
  * How do we do them? (Stop / start / continue, retro Google doc and/or posting on Slack for participation)
* Kanban Boards
  * link to GitHub Projects above?

## Key Assignments

* jpa00
  * Its purpose: getting started, ensuring students have working setups
* jpa01
  * Its purpose: introduction to Java, unit testing, mutation testing
  * Discuss how to autograde mutation tests (look for no survived, ignore timeout)
* jpa02 (first Heroku assignment)
  * Its purpose: introduce Heroku, get students to sign up and learn to deploy apps
  * Very small code changes
  * Discuss the autograder, how to autograde Heroku deployments
* jpa03 (setting up OAuth)
  * Its purpose: introduce the concept of OAuth, secret key values, GitHub Actions
  * How to grade this assignment (manual, rubric, things to watch for)
* team01
  * Its purpose: get students working on backend, creating REST APIs and working with external ones, introducing core git and GitHub concepts such as branching, kanban, pull requests
  * Grading: the autograder(s)
* team02
* team03
* Take-Home Final
  * What goes on it? Interview-type questions that demonstrate learning from this course

## Key In-Class Activities

* Early Career Software Developers Paper
  * Its purpose: to motivate this class, establish the problem, get students to think ahead to what they will get out of this class
  * Individual reading assignment, then group discussion
* Introductory Lecture Topics
  * A lecture on controllers, services, and Swagger UI
  * A lecture on unit and mutation testing
  * A lecture on React and component structure
  * A lecture on how to use Git branching and GitHub
* #help-lecture-discussion Help Queue
  * How does it work? (students post, staff react with emoji)
    * Showing the queue in the classroom
  * Expectations of the help queue
    * Start by being very lenient, gradually encourage / enforce more complex questions, similar to industry
* Brownfield Team Research
  * NSF Pre- and Post- Surveys
  * Informed Consent, how to introduce it
* Product Management / Ownership Activity
  * Its purpose: introduce how user stories are made, where they come from, the concept of talking to customers to develop feature
  * Comes with a lesson on product management in industry
  * Deep dive into existing applications, come up with issues
  * Staff will aggregate into epics for students
* Final Presentation Demos
  * Its purpose: provide a comprehensive overview of features that were worked on, establish a starting point for the next iteration of the class
  * Video submission on GauchoSpace
  * Video requirements, links to past videos

## Timeline

* A single-page document that links to other documents and provides a general timeline of when each thing should be introduced
* List of activities for initial class setup (before the first lecture)

## Staff Role

* Link to other places in the document, but provide an overview of how the staff is expected to support the students as time progresses
* A timeline for how to prepare and progress through the legacy code project
* How to mentor teams
* How to pick staff (?)

## Uncategorized / Miscellaneous

* How to use South Hall 1431
  * Benefits of the "active learning classrooms"
  * Table layout
  * How to use the lectern computer
* Differences between this course and CMPSC 148
* Suggestions for future work / tools
