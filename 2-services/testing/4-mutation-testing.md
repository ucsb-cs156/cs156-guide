# Mutation Testing

*Who tests the tests?* 🤔

Mutation testing is a technique for testing software in which the codebase is "mutated" to uncover hidden bugs. These mutations can take the form of a changed "if" statement, a changed boundary operator, or an empty return statement, for example. Mutation testing supplements existing unit tests; when code is "mutated", if one or more unit tests continues to pass, then the mutation "survives" and a potential bug is found. A successful mutation test run involves a run where all mutations are "killed" - that is, that every mutation made causes all tests to fail.

Mutation testing can also be seen as a way to validate existing code coverage results. As code coverage only checks if each line or branch of code is traversed by a unit test, it's possible for a codebase's code coverage to reach 100% without conducting any meaningful assertions. Since such unit tests would still pass within a mutated codebase, the mutation test run would fail, pointing out flaws in the designed unit tests. 

In CMPSC 156, we use [Pitest](https://pitest.org/) for Java Spring Boot mutation coverage, and [Stryker Mutator](https://stryker-mutator.io/) for JavaScript mutation coverage. Both frameworks can be run locally in a development environment through `maven` and `npm`. Additionally, mutation tests are run as one check within our GitHub Actions CI runs. As a result, PRs must include complete mutation coverage to be eligible to be merged.

## Pitest for Java Spring Boot

A list of Pitest mutators is available at <https://pitest.org/quickstart/mutators/>.

To run Pitest, execute the following command in the project's root directory:

```
mvn test pitest:mutationCoverage
```

This command will run the unit tests as-is first, then if they pass, run Pitest.

Pitest mutation test runs typically take a few minutes to run (will vary depending on hardware used). When the run finishes, a complete report is generated at `/target/pit-reports`. The `index.html` file can be opened in a web browser for viewing.

(Normally, Pitest will timestamp reports and place each report in its own directory with the path `target/pit-reports/YYYYMMDDHHMI`. This would allow for multiple reports to be saved until the next `mvn clean`. However, this has been disabled in [demo-spring-react-example](https://github.com/ucsb-cs156/demo-spring-react-example/blob/main/pom.xml#L186), so outputs of each run will replace previous runs.)

To run Pitest on only a specific Java class, add the following parameter:

```
-DtargetClasses=edu.ucsb.cs156.example.controllers.UsersController
```

Replace `edu.ucsb.cs156.example.controllers.UsersController` with your desired classes as a comma-separated value. Wildcard globs can be used here (e.g. `edu.ucsb.cs156.example.controllers.*`).

## Stryker Mutator for JavaScript (StrykerJS)

A list of StrykerJS mutators is available at <https://stryker-mutator.io/docs/mutation-testing-elements/supported-mutators/>.

To run Stryker, execute the following command in the project's `frontend` directory:

```
npx stryker run
```

Stryker will run Jest unit tests as-is first, then if they past, insert mutations.

Stryker JS takes a lot longer to run when compared to Pitest, especially on GitHub Actions, where we have seen runtimes of 40+ minutes. 

### Disabling Stryker Mutations

Occasionally, we will run into scenarios where it is necessary to exclude a line of code from mutation testing. Some React features / hooks have proven difficult for both students and staff to mutation test; to prevent projects from being held up due to mutation testing, staff can use their discretion to exclude blocks of code from being mutated.

We can insert the following comments to exclude a block of code from being mutated:

```
// Stryker disable all
{ code }
// Stryker enable all
```

Lines can also be excluded individually using this comment:

```
// Stryker disable next-line all
```

## Mutation Testing in Gradescope Autograders



