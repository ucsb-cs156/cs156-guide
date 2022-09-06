[Back to: 1-legacy-code-projects/0-outline.md](0-outline.md)

# Introduction to Legacy Code Projects

## What is a legacy code project?

One of CMPSC 156's main goals is to address the lack of "brownfield code development" in academia. Brownfield code development refers to development work on existing large-scale codebases, often designed to last and be built on for long periods of time. Most industry codebases exhibit brownfield development, where software developers focus their time on adding existing features to codebases that already exist, and are expected to continue to exist for an indefinite period going forward.

For purposes of this course, a "legacy code project" is a project that is maintained and iterated on by consecutive offerings of this course over multiple terms.

For the purposes of this documentation, the terms "brownfield code" and "legacy code" are synonymous.

## The Motivation (Why?)

Throughout a student's time in UCSB's Computer Science curriculum, they are asked to design many codebases as part of in-class labs, programming assignments, and class projects. Many of these codebases are purpose-built to teach core concepts using a *learn-by-doing* model. These codebases are often new, short-lived, small in size, and worked on by individuals or small teams.

These codebases are effective for building a solid foundational CS background, and such background can be useful in industry when learning to architect a new service. Yet, many junior / entry-level software developers struggle to fit in and make meaningful progress in their first few months in industry, facing issues with communication, collaboration, scale, and more. While existing computer science curriculum excels at teaching the algorithms and design principles used to build the widely-used systems in use today, it lacks the effective teaching of many soft skills vital to software development in industry.

For more motivation for this concept, see: [Listening to Early Career Developers (Craig et al., 2008)](https://pconrad.github.io/publication/028)

## The Current Legacy Projects

The current legacy code projects in use in CMPSC 156, as of the Spring 2022 quarter, are:

* UCSB Courses Search
    * A web app that utilizes UCSB APIs to provide additional functionality to the official UCSB Course Search applications.
* Happy Cows
    * A web app / game about grazing cows on a common farm designed to simulate the tragedy of the commons.
    
A candidate for a new legacy code project is this MVP developed by two former LAs for CMPSC 156:

* [Kanban Populator](https://github.com/brownfield-team/kanban-populator)
    * A web app that allows copying the contents of a Kanban board from one project to another.


Previous legacy code project include (but are not limited to):

* UCSB CS LAs
    * Formerly known as Tutor Scheduler and Open Lab Scheduler
    * A web app designed to facilitate the assignment of undergraduate learning assistants (ULAs) to classes and rooms for office hours.
* Mapache Search
    * A web app designed to analyze students' search and communication behaviors in computer science courses, developed in conjunction with an NSF grant.
