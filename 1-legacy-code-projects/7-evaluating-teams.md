[Back to: 1-legacy-code-projects/0-outline.md](0-outline.md)

# Evaluating Student Teams

One of this course's main challenges is finding an efficient and fair way to evaluate team performance for the purposes of assigning a grade. As different student teams are assigned different epics with varying levels of difficulty, it is impossible to come up with a one-size-fits-all objective rubric.

In aligning with our mission to introduce students to professional software development practices, we incorporate a "story point" system similar to those used in professional Agile teams, but modify it to fit an academic environment (i.e. to be graded).

## The Point System

We use a modified "story point" scale based on multiples of five. Most issue / pull request combinations are assigned values of 5, 10, or 20 points, with higher point values being assigned for more challenging features. Each team's goal in the project phase is to obtain 100 points by collectively completing / merging pull requests. Teams additionally have the opportunity to earn 10 extra credit points, up to a maximum of 110 points.

Unlike story point usage in industry, however, the process of assigning point values is done *after the pull request is merged*, and values are assigned based on the *actual* effort put in to the story, as determined by the PR's staff reviewer.

Typically, point values are typically assigned based on the following guidelines:

| Points | Description |
|--------|-------------|
| **5** | Pull requests that contain trivial changes that do not require much thought. This point value is mostly reserved for initial setup tasks, starter stories, and minor bug fixes. |
| **10** | Code-complete pull requests for smaller / minor features, or partial implementations of larger / major features. |
| **20** | Code-complete pull requests for larger / major features. |

Occasionally, staff may come across pull requests that are particularly outstanding or complex that warrant more than 20 points and can otherwise not be broken up into smaller pull requests. Such PRs should have pristine attention to detail in terms of user interface, backend design, and code / test structure. Staff should confirm with the instructor before assigning this point value.

## Assigning Point Values

Because point values being assigned *after* an issue is completed, and based on the contents of the actual code merged in, assigned point values are subjective and often rely on staff's past knowledge working on codebases. This may occasionally result in discrepancies between what the team expects to earn for a given issue and what the staff ultimately assigned.

If a staff member is uncertain about the point value of a PR, they can always delegate that task to the instructor. If there is still uncertainty, **staff are advised to always underestimate the point value** (i.e. assign the lowest earned point value). It is always easier to underestimate a value and then increase it later, than to overestimate a value and then decrease it later. We never want to be in a position where we have to decrease a team's grade on a pull request. 

In situations where a team feels they have not been assigned an adequate point value for their work, they have the option to "contest" their grade through the instructor. Such requests should be discussed in person whenever possible and involve a team-wide conversation of what their desired grade is and why they believe it should be higher. These requests are generally only considered if the team is able to show that there was extensive work outside of the PR that was done to make it happen, such as the time spent learning and optimizing a new API, tool, or library.

It is always helpful to remind students of the known uncertainties of grading in this phase of the course. A simple Slack announcement, like the below announcement from Spring 2021, will suffice: 

> We determine the point values after the PRs are made based on the amount of effort required to complete the stories. Most of these stories are between 10 and 20 points but we are not able to give a concrete point value until after they are completed. We wish we could tell you in advance, but the difficulty with this type of programming is that we have no reliable way to estimate point values before they are finished.

## Handling Issues of Individual Student Performance

Points are collectively earned as a team, not as an individual. Students should notify their instructors of any inter-team issues as early as possible to make amends, but often, students wait until far too late into the process to report such issues. As a result, we utilize the CATME Peer Evaluation system to handle these cases.

If a student feels that one or more members of the team are not performing to the same degree as others in the same team (including themselves), the team will still accrue project points together, but they will have an opportunity to make that known through CATME peer evaluation surveys. **The aggregate score of the final CATME survey will be used as a percentage multiplier for a student's project score**, so students with a lower multiplier will see their final project score decrease.

As always, individual grading issues should always be resolved through the instructor - TAs and ULAs should not be handling these requests.
