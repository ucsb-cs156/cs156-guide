[Back to: 1-legacy-code-projects/0-outline.md](0-outline.md)

# The Development Lifecycle

In most of academia, students write and deploy code directly to a single "production" environment that they submit at the end of the project. This is the case with our individual JPA assignments, as students are working on and deploying to a single Heroku environment throughout the entire assignment. 

However, in many professional environments, implementing changes directly to production environments is heavily frowned upon / restricted, due to its potential to cause issues down the line. By circumventing normal review procedures, the opportunities for bugs and regressions to appear increase, and end users will have a degraded experience using the application, which has the potential to hurt the application maker's reputation. 

(This is why there are a plethora of memes about "debugging in production" - it's extremely risky, so try to avoid it whenever possible!)

As a result, many projects establish a "development lifecycle" with different deployment stages to allow for adequate testing and validation before a change gets pushed to an end user. These often take the form of one or more QA environments between the beginning of the lifecycle - the development stage - and the end of the lifecycle - the production environment. Such environments can go by many names, including Alpha / Beta / Gamma, Canary, and Staging.

In CMPSC 156, we aim to keep things simple while providing the full experience, so we use only utilize one QA environment. The three environments in the lifecycle are:

1. The Development Environment
    * This is the developer's own computer with their own development tools installed. While we attempt to standardize this environment through minimum software versions, this environment is often not consistent across development machines due to the nature of the course.
2. The Quality Assurance (QA) Environment
    * This is a standardized "production-like" environment, meaning it's deployed in the same way the actual production environment would be, but in a non-customer-facing area only accessible to development teams where changes can be tested before finally being merged in.
3. The Production Environment
    * This is the main environment serving production traffic (i.e. traffic from actual end users / customers of the application). In this stage, bugs should be minimal, and major changes should be minimized. Any stateful data is expected to be persistent at this stage.

## Introducing The Development Lifecycle

### Heroku QA and Production

The development lifecycle is first introduced to students through team01 - the first team programming assignment. As part of the assignment, teams are instructed to create **two** Heroku deployments (as opposed to the usual one):

* a "production" Heroku environment, with automatic deploys enabled
* a "QA" Heroku environment, suffixed with `-qa`, with manual deploys

team01 is also the assignment where students are first introduced to git branching and GitHub pull requests. Through lecture material, students are taught how to navigate the pull request workflow, including how to review other students' code. As part of learning to review code, students are encouraged to deploy the developer's changes to their shared Heroku QA deployment and use the developer's provided test plan to validate their changes. Only when changes are verified using this manner, are changes allowed to be approved and merged into main.

As a result of this process, students should not need to manually configure / deploy the production environment after it's been initially set up. Given that any code changes has been previously reviewed in QA, the production environment is expected to be bug-free. This is what will ultimately be tested against in the team01 Gradescope autograders.

Students are asked to continue the practices of establishing a QA and Production environment, deploying to QA during code review, and demoing the Production environment, in all future assignments including the legacy code project. 

Information on how to set up Heroku QA and Production environments can be found in [Deploying to Heroku](../2-services/heroku/3-deploying-to-heroku.md#production-and-qa-deployments).

### Storybook QA and Production

The development lifecycle is further introduced to students through team03, which is the first team programming assignment to feature frontend development. In learning how to develop frontend user interfaces using React, students are introduced to Storybook, a tool allowing components to be isolated for UI development purposes.

Like any React website, Storybook pages have the ability to be compiled down into static webpages for deployment to a hosting service. In this class, we have established tools to automate the deployment of Storybooks in our apps to a separate repository for GitHub Pages hosting. As part of the assignment, teams are instructed to create **two** "docs" repositories for Storybook deployments:

* a "production" Docs repository for Storybooks built from the `main` branch
* a "QA" Docs repository for Storybooks built from any other branch

Aside from initial setup of a `DOCS_TOKEN`, students don't have to do any additional work to get Storybooks built in these environments. Pull requests will automatically generate a Storybook in the QA environment, and merges to the `main` branch will automatically update the production Storybook. Students are encouraged to link to Storybooks in pull requests to use it as a validation tool, furthering the notion of the development cycle within the course.
