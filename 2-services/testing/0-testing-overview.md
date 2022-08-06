# Testing

Most, if not all, professional software teams incorporate some sort of testing into the products that they build and maintain. Testing is crucial to ensuring that all parts of an application work when deployed, and can act as a first point of defense for any issues that arise during development.

Here are some of the types of testing used in professional teams:

* **Unit Testing**

  This is the act of testing individual methods (i.e. small "units") in code to verify that every unit, when tested independently, works as expected. This is the lowest level of testing and runs using frameworks within the language itself. 

* **Mutation Testing**

  This is the act of "testing the tests". Mutation tests are not explicitly written by developers; instead, mutation tests introduce small changes  known as "mutations" into existing unit test suites, with the expectation that such small changes will cause test suites to fail, i.e. "survive". These tests serve as an indicator of incomplete unit testing, which can prevent hard-to-find bugs in a larger application.

* **Integration Testing**

  This is the act of testing multiple components of an application together to ensure that they can cooperate without issue. As the functionality of individual components has already been verified through unit tests, these tests focus on interoperability and often require launching multiple services.

* **End-to-End Testing**

  This is the act of testing entire user / feature workflows end-to-end, just like a user would in normal usage of the product. This is the highest level of testing, and can be done by either an automated testing framework or dedicated QA / Testing engineers.

There are many other types of software testing, but the above are the most commonly used types of testing that our course staff have encountered, and are the ones that we introduce to our students. This article from [Atlassian](https://www.atlassian.com/continuous-delivery/software-testing/types-of-software-testing) is one such resource for types of software testing.

## Unit and Mutation Testing in CMPSC 156

In CMPSC 156, we enforce complete and thorough unit testing of all code written, as part of our efforts to introduce software development practices in industry. Codebases are presented to students with complete (100%) test coverage, and in both programming assignments and the legacy code project, students are expected to maintain complete coverage within the codebase. 

Every language / framework used within our legacy code projects has a corresponding testing framework - our backend Java Spring Boot code is tested using *JUnit* and reported using *Jacoco*, and our frontend React code is tested and reported using *Jest*. To aggregate and track these results, we use *Codecov*, which works with CI providers such as GitHub Actions to neatly present and enforce code coverage in GitHub repositories.

We additionally make use of mutation testing to enhance our unit test suite, through the use of *Pitest* for Java and *Stryker* for JavaScript. 
As mutation testing is used to detect inadequate unit testing in a project codebase, mutation testing helps students to gain a better understand of any code they may write, and serves as a motivational tool for students to adopt the test-driven-development (TDD) methodology, where failing tests are written before actual development work occurs.

The introduction of complete unit testing, code coverage, and mutation testing, is mainly thanks to work done by Scott Chow as part of his Masters project, "Teaching Testing with Modern Technology Stacks in Undergraduate Software Engineering Courses". Other CS 156 students have built on Scott's work, including Jayleen Li and Cole Bergmann.

*(Link Scott's paper or presentation here maybe?)*

## Manual End-to-End Testing in CMPSC 156

We do not yet have automated integration or end-to-end testing in our codebases, and as such, they are not taught hands-on in CMPSC 156. (There have been past efforts to add this in though, through tools such as Cypress, which can end-to-end test JavaScript web applications.)

However, we encourage *manual end-to-end testing* as part of the pull request process. As part of the pull request template, developers are encouraged to write out a "test plan" for new features, which is a series of steps that a user can take within the application to test a newly-developed change. Code reviewers are then expected to test such plans / functionality using Heroku QA deployments before merging. This allows students to be involved in the QA process, giving students a small introduction into the much larger QA processes in industry.
