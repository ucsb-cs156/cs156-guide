# Codecov

Codecov is a service that aggregates code coverage metrics for software codebases. The product allows users to see, store, and track code coverage from a variety of languages and testing frameworks, and use these metrics to provide insights and enforce checks. Through its GitHub integration, Codecov can automatically gather code coverage data from GitHub Actions CI runs, provide coverage reports directly in pull requests, and prevent code merges if coverage thresholds are not met.

In enforcing code coverage thresholds, Codecov reports two types of statuses: "Project" statuses, which compares overall project coverage, and "Patch" status, which only looks at code coverage for changed lines in a pull request.

## Codecov in CMPSC 156

Codecov is used in CMPSC 156 to:

* View code coverage of repositories on GitHub

  Codecov can be used to present coverage results for repositories hosted in GitHub, eliminating the need to clone a repository and run a test suite manually. Additionally, since Codecov stores all uploaded code coverage reports, code coverage in a repository can be tracked over time.

* Combine test coverage results from our Spring Boot backend and React frontend Actions runs into one unified, user-friendly view

  Since our codebase features different languages / frameworks for frontend and backend code, tests for each remain independent of each other. While this can be useful in development, it can be hard to analyze the overall codebase's coverage in production or in code review. Codecov is able to aggregate the coverage reports from both Jacoco and Jest into a single report with a user-friendly website.

  ![Codecov Sunburst](../../images/services/testing/codecov-sunburst.PNG)

* Provide summarized coverage reports inline in GitHub Pull Requests

  With Codecov's GitHub integration, once a pull request's coverage CI runs have completed, Codecov can post a summary of the pull request's changes and code coverage as a comment inline in the pull request review thread. This allows reviewers to easily glance at the coverage of changes being reviewed.

  ![Codecov Summary](../../images/services/testing/codecov-pr-summary.PNG)

* View dropped coverage inline using GitHub's diff view

  In addition to proving the above PR summary, Codecov is also able to add inline code review comments on places with incomplete coverage.

  ![Codecov Diff Comment](../../images/services/testing/codecov-pr-diff-comment.PNG)

* Enforce coverage thresholds for individual PRs and entire repositories

  Codecov performs two types of status checks:

  * "Project" checks, which look at the entire codebase's code coverage
  * "Patch" checks, which only look at the coverage of changed lines

  For each one, Codecov allows project owners to enforce a coverage threshold. This threshold value indicates the allowed percentage drop for each check that will constitute a "passing" check, when compared to the coverage of the base of the branch. 

  Repositories in this class use the [default Codecov settings](https://docs.codecov.com/docs/commit-status) and therefore do not have a `codecov.yml` file defined. The default settings define a 0% coverage diff threshold for both checks, which means that *any* drop in coverage will result in a failed check in pull requests.

  ![Codecov Status Checks](../../images/services/testing/codecov-pr-status-checks.PNG)

* Provide a code coverage badge in project READMEs

  A clickable badge, like the one below for demo-spring-react-example, can be added to a project's documentation or README as an easy way to access Codecov coverage reports.

  [![codecov](https://codecov.io/gh/ucsb-cs156/demo-spring-react-example/branch/main/graph/badge.svg?token=vT8pDxc6Fo)](https://codecov.io/gh/ucsb-cs156/demo-spring-react-example)

## Codecov and the GitHub Student Developer Pack

Codecov is free for open-source (public) projects. but is paid for private projects if more than five users are needed. However, Codecov is part of the [GitHub Student Developer Pack](https://education.github.com/pack), and verified students won't occupy any seats within a Codecov organization. As a result, **students will need to register for the GitHub Student Developer Pack before using Codecov**. Teachers, however, will continue to take up a slot, even if registered as a faculty member through GitHub, as educators do not get the same benefits.

To ensure that we do not exceed our private user quota reserved for staff without a student affiliation, **staff will need to manually validate students** as they register for Codecov to make sure they have correctly signed up. We make use of the [#help-codecov channel](../slack/3-channels.md#help-codecov) in Slack to facilitate such requests to activate students.

Instructions to validate students are listed in the [Codecov Initial Setup document](3-codecov-initial-setup.md). 

## Setting Up Codecov Repos

### Default Branch

### GitHub Actions `CODECOV_TOKEN` for private repos

### Codecov README Badge

