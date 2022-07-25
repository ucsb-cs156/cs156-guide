# Issues and Epic Planning

GitHub Issues allows project teams to track work that needs to be completed for a linked project. Individual issues can be filed by developers to suggest new features and fix existing bugs, and groups of related issues can be grouped together into "epics" using Milestones or GitHub Projects. Issues is heavily integrated into the GitHub workflow and provides functionality comparable to other professional issue management and ticketing tools used in industry, such as Jira.

In CMPSC 156, students will play multiple roles when it comes to managing an issue backlog. Students will act not only as developers looking to resolve issues through code changes, but also as product owners and managers, creating new issue requests based on "customer feedback" in deep dives of the legacy code project. 

## Types of Issues / Issue Templates

Generally, issues within legacy code projects fall into three categories:

* Feature Requests / User Stories
* Bug Reports
* Code Refactor Requests

The majority of issues created in this course will fall under the first category. As part of a class activity on product management and product ownership, students will be advised to act as customers and file feature requests for tools that they believe are essential to improving the quality and usefulness of the product that they will be working on. This feedback will be used by the staff to form a set of epics and their related issues, which will be distributed to student teams.

To ensure that such issues are fully detailed for the developer, we establish issue templates for the three most common types of issues listed above. These issue requests standardize the issue creation process while encouraging students to think like a product owner.

Each issue template contains the following:

* Feature Requests
  * A description of the feature in user story format
    * As a _____, I can _____, so that _____.
  * A longer discussion of the feature
    * This is a place for any supporting documentation, such as mockups or design considerations.
  * A checkbox list of acceptance criteria
    * Statements that should be true when the story is complete
  * A checkbox list of implementation TODOs, separated into sections for frontend, backend, and testing.
* Bug Reports
  * A short description of the bug
  * A comparison of what the expected behavior is and what actually happens
  * An ordered list of steps to reproduce, along with information about the runtime environment
  * Any supporting error messaging, screenshots, links to relevant lines of code
* Refactor Requests
  * A description of the part(s) of code to be refactored
  * A checkbox list of acceptance criteria
    * Statements that should be true when the story is complete
  * A checkbox list of implementation TODOs, separated into sections for frontend, backend, and testing.

Examples of issue templates are viewable in [this GitHub repository](https://github.com/alu-classroom-test/.github). These are slightly modified from the Spring 2022 instance of CMPSC 156.

Issue templates can be set up at the organization level, and the setup instructions can be found on the [GitHub Initial Setup page](../2-services/github/2-initial-setup.md#step-6-establish-organization-wide-issue-and-pull-request-templates).

## Starter Issues

In addition to the above types of issues, we also establish a special designation for "starter" issues. These issues are **small, trivial issues designed to ease students into the legacy project codebases**. Through this process, students will familiarize themselves with the structure of the codebase, with the goal of being able to identify where in a codebase a new feature must be added. Students are also able to practice the formal deployment and pull request processes set in place, such as required testing and code coverage, reviews from team and staff, and linked issues / Kanban board management.

Each team should be assigned enough issues such that there is at least one issue per every two students on the team. This allows team members to pair on the starter issues, overcoming any challenges as a pair before proceeding to work on larger issues on their own.

Historically, most "starter" issues have been frontend UI changes, mostly one-liners. These are the easiest to perform, since they do not require extensive knowledge of backend architecture and the underlying algorithms.

The following issues are examples of good starter issues:

* Standardize input field names on a form (capitalization, grammar)
* Change the title of a React page
* Make a table column sortable
* Replace a website favicon or logo
* Adjust spacing of various website components
 
The starter issue workflow was last used in Spring 2021, when legacy code projects were assigned to specific sections, and each team had their own unique epic. A specific "starter" label was used to designate such stories. Do NOT use GitHub's built in "good first issue" label - this makes tagged issues publicly available / searchable!

Starter issues from the 2021 versions of legacy code applications can be viewed here:

* [UCSB Courses Search](https://github.com/ucsb-cs156-s21/proj-ucsb-courses-search/issues?q=is%3Aissue+label%3Astarter)
* [UCSB CS LAs](https://github.com/ucsb-cs156-s21/proj-ucsb-cs-las/issues?q=is%3Aissue+label%3Astarter)
* [Mapache Search](https://github.com/ucsb-cs156-s21/proj-mapache-search/issues?q=is%3Aissue+label%3AS21-Starter)

In the current class setup, where there are two legacy code projects with two epics each, and each epic is replicated three times (once in each section), starter stories have been replaced with clerical setup tasks instead, such as establishing the Prod and QA lifecycle on Heroku and Storybook, generating any necessary authentication tokens, and setting up Codecov. If we are able to rearrange team projects to start earlier and allow more legacy code project time, this is one aspect that could be re-introduced.

## Epic Creation



