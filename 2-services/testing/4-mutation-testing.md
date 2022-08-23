# Mutation Testing

*Who tests the tests?* 🤔

Mutation testing is a technique for testing software in which the codebase is "mutated" to uncover hidden bugs. These mutations can take the form of a changed "if" statement, a changed boundary operator, or an empty return statement, for example. Mutation testing supplements existing unit tests; when code is "mutated", if one or more unit tests continues to pass, then the mutation "survives" and a potential bug is found. A successful mutation test run involves a run where all mutations are "killed" - that is, that every mutation made causes all tests to fail.

Mutation testing can also be seen as a way to validate existing code coverage results. As code coverage only checks if each line or branch of code is traversed by a unit test, it's possible for a codebase's code coverage to reach 100% without conducting any meaningful assertions. Since such unit tests would still pass within a mutated codebase, the mutation test run would fail, pointing out flaws in the designed unit tests. 

In CMPSC 156, we use [Pitest](https://pitest.org/) for Java Spring Boot mutation coverage, and [Stryker Mutator](https://stryker-mutator.io/) for JavaScript mutation coverage. Both frameworks can be run locally in a development environment through `maven` and `npm`. Additionally, mutation tests are run as one check within our GitHub Actions CI runs. As a result, PRs must include complete mutation coverage to be eligible to be merged.

## Mutation Testing in Legacy Code Projects



## Mutation Testing in Gradescope Autograders



