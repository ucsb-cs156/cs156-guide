[Back to: 1-legacy-code-projects/0-outline.md](0-outline.md)

# Common Pitfalls

Staff often see students make the same mistakes in each iteration of the course. This document aims to outline some of those, along with how they are typically resolved, so staff can easily detect and avoid them in the future.

## Making code changes directly in the GitHub web editor

**Students should never make code changes directly in the GitHub web editor, especially when working with credentials**. This includes VS Code for Web ([vscode.dev](https://vscode.dev/) and [github.dev](https://github.dev/)). Using web editors are only recommended for note-taking and editing Markdown files such as READMEs.

There are a few reasons why this is a discouraged practice:

* **Web editors are NOT code execution environments**, and as a result, are not able to run applications or test suites. Changes should always be tested before they are committed / merged, and students should NOT be using CI test workflows as a replacement for local environment testing. 
* Web editors, especially the one built directly into github.com, **bypass the .gitignore file, which can lead to leaked credentials**. Credentials of any sort should NOT be handled through GitHub's web interface, unless it's specifically adding an environment secret in the Settings panels. If a credential is leaked in this manner, regardless of whether it is eventually removed, it should be invalidated and rotated immediately.
* GitHub's default web editor only allows you to edit one file at a time, leading to **lots of tiny commits with poor commit messages**. This unnecessarily clutters up a commit log and makes it harder for developers to (a) understand what is occurring, and (b) trace bugs and issues in the future.

If a student is in a position where they do not have access to a local development machine (e.g. a broken, lost, or stolen computer), they can always fall back to using CSIL as their development environment. If CSIL becomes a constraint due to poor performance with Node, they can work with the course staff to look into cloud-hosted alternatives, such as GitHub Codespaces or AWS instances.

The following Slack message from Spring 2021 outlines the above point fairly well (slightly edited for clarity):

> A note: we've used the GitHub web interface for editing documentation and text, and that's fine. But: using the GitHub web interface to edit your **code** is generally considered **bad practice** for several reasons:
> 
> * First, it is dangerous if you are editing credential files such as `secrets-localhost.properties` that are supposed to be ignored by `git` because they appear in your `.gitignore`. Editing directly in the git web interface bypasses these protections and can cause secret information to leak. **Definitely never do this.**
> 
> * Second, **read the bullet item above again.** It's super important to NOT edit files containing Auth0 or Google credentials through the GitHub web editor.
> 
> * Third, when you edit code directly in the GitHub web interface, then the only way that code is getting tested is via the CI/CD servers, and on Heroku. This is wasteful: you are firing up the entire testing suite on a complimentary cloud platform to test one tiny change at a time. CI/CD is intended as a backstop, the place where you test your code last, not first.
> 
> * Finally: it results in a git history of dozens of tiny changes, each of which likely has a poor commit message, and is just "churn". That's a big tell for a future employer: this person doesn't really know what they are doing yet.
> 
> What should you do instead? Clone the repo, and edit it on your file system. Test your changes on a local system first (your own computer or CSIL), and only once they are working and you are confident that you have a good commit for some unit of working code, then make a commit with a good commit message.
> 
> TL;DR... editing through the GitHub web interface should be for text changes only, not code changes and NEVER for credential changes.

## Students thinking they can't make progress while a PR is awaiting review

Another issue that comes up often is that students state they are "blocked" waiting for a PR to be merged in, sometimes due to a missing staff review. While it can be easier to write all your code in a linear fashion and not have to deal with merging and rebasing, this workflow is unsustainable, especially given the number of teams that each staff member has to review for alongside their normal commitments outside of class.

Instead, if a student wants to start work on a new issue that is dependent on a PR that is currently in review, encourage students to **branch off of the branch being reviewed** and continue building out their feature set. If changes need to be made to the original branch, simply switch back to that branch, make the change, and then push it back in for review. Once the initial branch is finally merged into the main branch, simply rebase the new branch off of the `main` branch, and any new work will be pulled in to the new development branch.

The situation gets more complicated if a new feature is dependent on multiple, unrelated branches, however. In this scenario, to save students and staff the trouble of resolving issues later on, it is more advisable to prioritize reviewing the original PRs instead.

## One Giant PR (as opposed to multiple smaller PRs)

One practice followed by Agile teams is that of **iterative development**. This means that teams should break large features into smaller issues and merge smaller chunks of code more frequently, often following a cycle. This is as opposed to building out an entire feature and waiting to merge it in all at once.

While this approach may not work for some professional software development teams due to the nature of the product being built, the legacy code projects in this course are not mission-critical and allow for occasional hiccups and adaptations to change.

There are a few benefits to the iterative approach:

* Smaller PRs are **easier to review**. There is less code to be analyzed and tested in each PR, which leads to faster turnaround times and less stale code.
* By breaking down large features into smaller PRs, each with their own descriptions, tracing a bug's origin is much simpler.
* Frequent, small PRs **reduce the potential for merge conflicts**. Merge conflicts often result in PRs that are both large and stale, and iterative development solves both of those issues.

**Staff can, at their discretion, refuse to review a PR that addresses multiple issues and/or is otherwise too big**. In this scenario, students should be instructed to separate out their code into multiple smaller PRs, and staff should guide the student(s) through the process.

## Remaking PRs after changes requested in a code review

For some students, the legacy code project will be the first time they will have a change requested as part of a code review. This can be due to the fact that the initial team assignments are designed to be straightforward and often involve little oversight from the staff. As a result, however, students may not know how to handle situations where they need to submit another revision of the code, and as a result, opt to close the original pull request, make their changes, and then create an entirely new request with the changed code.

Staff should reiterate to students that, in this situation, **students should NOT re-create their pull requests. Students simply need to push new commits to the branch**. A pull request will automatically update with new changes, and students will be able to re-request the previous reviewers.

Remaking pull requests has a few other drawbacks as well:

* **Any previous pull request comments are lost**. Pull request feedback does not transfer over if a pull request is remade in this fashion, which can lead to a loss of context and ultimately delay the review process.
* **New pull requests are assigned a new number**. This will not only cause more delays, as staff will likely review pull requests in the order they are made, but also introduce issues if earlier pull requests depend on changes that were remade in the later PR.
* The pull request log is unnecessarily cluttered.

## Students do the wrong thing well (Avoiding predictable outcomes)

In an academic setting, students tend to focus more on *correctness* rather than *completeness*. This mentality makes sense in most other courses, where programming assignments serve a specific purpose, and it is generally always better to focus on making existing code correct as opposed to writing new code. However, in CMPSC 156, **this mindset will often lead to students writing code of excellent quality that serves no meaningful purpose in the actual application**. This is indicative of a disconnect between the development teams and the end users.

One example of this scenario that has occurred multiple times in Spring 2022 is the Happy Cows leaderboard. Given a set of users and the amount of money each one has, a leaderboard is simply the list of users sorted by their wealth. The wrong approach taken by students, however, was to create a separate "Leaderboard" table holding user rankings.

These issues can be avoided by encouraging **consistent communication between students and the course staff**. Vagueness and ambiguity are baked into many levels of this course by design, and students are encouraged to work through such issues through issue clarification with their assigned mentors and through public Slack help channels. (Side note: being able to work through these scenarios is a helpful life skill! It was the main area of concern in my first internship).

Additionally, **"issue grooming" exercises** may help alleviate this issue. By allowing students to flesh out their own user stories, requirements, and acceptance criteria, students are encouraged to seek out a deeper understanding of the product as a whole, and play the role of the customer.
