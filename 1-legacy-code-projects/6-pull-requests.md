[Back to: 1-legacy-code-projects/0-outline.md](0-outline.md)


# Pull Requests

Pull Requests are GitHub's mechanisms for performing code reviews. If a user wants to merge newly-developed code from a feature branch into an upstream branch (in our case, the `main` branch), they will open a pull request where code reviewers will have the opportunity to make comments, request changes, and/or grant approvals.

In supporting our efforts to provide first-hand experiences of the software development practices used in industry, we enforce Pull Requests for all team assignments and the legacy code project. Pull request requirements and complexity gradually increase as the course progresses, with the expectation that students will be held to the same standards as staff when contributing to the legacy code project at the ending phase of the course.

## The Pull Request Template

Like code reviews in industry, pull requests must be accompanied with a description that explains to the code reviewer (and any future developers looking back) what they're about to look at. This is a place for a developer to provide any necessary context for a code reviewer to understand, test, and validate the code in question. This is especially useful in larger organizations, where developers can be unaware of what is being worked on.

In CMPSC 156, we establish a pull request template to provide structure for descriptions in all pull requests. Specifically, the pull request template asks developers to input the following:

* An overview of the changes made
  * This should describe the impact of the change for the customer
  * If the issue was a user story, students are asked to repeat the user story format here.
  * If the issue was a bug, then students are asked to show a before and after comparison
* A list of the issues to be resolved, with closing keywords
  * Closing keywords, such as `Closes #1`, allow GitHub to automatically link a pull request to an issue.
  * Linked issues should also be fleshed out / have proper documentation
* Links to Storybook components (if the PR includes frontend changes)
* Application screenshots, if applicable
* An ordered list of steps to test the changes made (i.e. a "test plan")

A sample GitHub Pull Request template is viewable [here](https://raw.githubusercontent.com/alu-classroom-test/.github/main/.github/PULL_REQUEST_TEMPLATE.md). This is slightly modified from the Spring 2022 instance of CMPSC 156. Full setup instructions for issue and pull request templates can be found in [GitHub Initial Setup](../2-services/github/2-initial-setup.md#step-6-establish-organization-wide-issue-and-pull-request-templates).

In team assignments, students are encouraged to use the template when submitting pull requests for team members to review, but are not strictly graded on the content of their pull request descriptions. In the legacy code phase of the course, however, staff are instructed to reject pull requests with insufficient descriptions, as they lack the necessary background to be reviewed. The burden is not on the staff to figure out what a student has completed.

## Things to look for in Pull Requests

There are many components that compose a good pull request that is ready to be merged. These guidelines apply to both team assignments and legacy code projects.

### Pull Request Hygiene:

* Pull requests should have **descriptive titles and descriptions**

  The title should be a very minimal description of the implemented / fixed feature, even shorter than user story format. This is simply to allow a reviewer looking through a pull request log to easily identify a PR.

  The description is where students are asked to be detailed. This will involve filling out the information presented in the template above, including a description of the story, its impact on the end user, the changes that were made to resolve it, and any helping screenshots or deployments.

* Pull requests should **list who contributed to the code** being reviewed in the "Assignees" section

  This allows reviewers to know who worked on the code being reviewed. This gives the reviewer a point of contact for any questions, as well as credit to the authors of the code. Multiple assignees can be listed here.

* Pull requests should have at least **two approving reviews from members that did not work on the issue**

  In team assignments, these two reviews will come from within the team. In the legacy code phase, one of these reviews will come from within the team, and another will come from a member of the course staff, who will ultimately merge the code.

* Pull requests should be **linked to the issue(s)** they resolve, and **linked issue(s) should be properly groomed**

  Issue linking can be done manually in the sidebar or through a [closing keyword](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue#linking-a-pull-request-to-an-issue-using-a-keyword) in the PR description.

* All GitHub Actions checks should **pass with a "✔"**

  GitHub Actions is our CI provider and serves as the last layer of defense for code that does not pass project tests. These checks include:

    * Java JUnit testing and Pitest mutation coverage
    * JavaScript Jest testing and Stryker mutation coverage
    * Code coverage for the above using Codecov
    * Production Build Check
    * Storybook Build and Deploy Check

  **Failing tests should never be merged into the codebase**. Dropped code coverage is also generally not acceptable, but may be allowed in very certain cases at instructor discretion. In cases where the instructor finds a piece of code very challenging to cover, exclusions should be made in the code to avoid a reported drop in coverage.

* Pull requests should have the **team label** added

  This applies only for legacy code project PRs, and is the way pull request points are attributed to teams. Instructors can determine a group's points by using the following search query and counting all point label values.

  ```
  is:merged label:s22-4pm-1
  ```

* Commit messages in the branch should be descriptive

  Students should give descriptive commit names for all commits they make. This makes it easy for future developers to traverse the commit history to identify bugs and learn about changes in the codebase. While this item can be challenging to enforce, students should be encouraged to use clean commit message names whenever possible, and staff reserve the right to deduct points if necessary.

### Reviewing Code:

* Code changes should **not contain undesired files, especially credentials**

  Occasionally, students will use `git add .` to stage their changes without actually being aware of what's being added. This can sometimes lead to unwanted or unrelated changes being added, especially in `package-lock.json` and with `.env` credential files. Such changes should be removed, and if the change contains credentials, those credentials should be immediately invalidated as these repositories are public.

* Pull requests should be **free of commented code**

  Commented code should only be present in the codebase if it serves a specific and documented purpose. Any commented code lines / blocks that are not accompanied by a description should be removed.

  It may be helpful to implement the `no-commented-out-code` ESLint rule suggested by Bryan Terce that checks for this case. [Documentation here](https://github.com/cartant/eslint-plugin-etc/blob/main/docs/rules/no-commented-out-code.md)

* Code logic should be **sensible and easy to follow**

  This involves checking to make sure the issue is approached in a correct and straightforward manner. For example, an issue about a course backend API route should probably not be pulling a list of app users. This also includes ensuring that variable names are descriptive of the variables they hold and that code is properly formatted to ensure consistency.

* Test data should be **free of any identifiable information**

  If a test is meant to mock user or class data, for example, it should not contain information that is otherwise considered private. This includes student names and emails and class Zoom links, for example.

* Reviewers should **deploy the app to Heroku QA to ensure functionality**

  This is to ensure that the issue is resolved as intended and works end-to-end. While tests will generally catch small issues, larger functionality issues are hard to catch without extensive testing. If a test plan is included in the PR description, the reviewer should be able to follow it without issue.

* Any code review comments should be resolved before merging
