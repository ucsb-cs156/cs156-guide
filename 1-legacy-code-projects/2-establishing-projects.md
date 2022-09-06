[Back to: 1-legacy-code-projects/0-outline.md](0-outline.md)

# Establishing Legacy Code Projects

## How do we choose legacy projects?

In choosing legacy code projects for CMPSC 156, we look for a few criteria:

1. Customer / User Base

    One important aspect of software product development is the need to constantly evaluate your customers' needs and wants and develop based on that. Industry projects typically have customers that they need to serve, but that is challenging to find in an academic environment. 
    
    To resolve this, we look for apps where *the students themselves are the target customers* - in other words, apps that students would use themselves. This allows us to carry out exercises where students "interview the customer" to determine user stories and flesh out project requirements.

2. Size / Scope

    Industry projects are often supported by multiple teams at once, especially those found in larger companies with established products. These projects should be large enough in scope such that there are multiple features that can be developed in parallel by multiple student teams. 

    In CMPSC 156, we often assign projects to sections, meaning each section of the class acts as one organization developing for that product. Each section is then usually split into four teams of six students, all of which will have their own feature epic in the legacy code phase of the course.

3. Long Term Support

    Many industry products are designed to last for years on end, and their codebases must be supported as such. Since industry employees often come and go, these codebases are often structured, tested, and documented. We aim to achieve this by supporting products that will be used well into the future.

4. Tech Stack

    While it is common to use the newest frameworks and languages in greenfield code development, brownfield projects, especially those that have already been established for multiple years, either already have an established tech stack or require a specific tech stack to maintain compatibility with another software projects.

    Currently, all CMPSC 156 projects feature a Java / Spring Boot backend and a JavaScript / React frontend. While this tech stack has been revised a few times in recent years, the core language of the tech stack, Java, has been carried down through all iterations as implied in the course description.

    Tech Stack Timeline:
    * Pre-F19: Java desktop applications using Swing GUI
    * F19 - W20: Java 11 web applications with Spring Boot backend and Thymeleaf frontend
    * F20 - S21: Java 11 web applications with Spring Boot backend, React frontend, and Auth0 authentication
    * W22 - current: Java 17 web applications with Spring Boot backend, React frontend, native Spring OAuth

## How do we choose the technologies that we use in this course?

The only "official" requirement for the technology stack used in this course, per the UCSB course description, is that Java is used to some degree in this course. This requirement has dated long before the course shifted focus to web apps.

However, this course has evolved to be much more than just "Advanced Applications Programming" - this course now focuses on exposing students to professional software development practices in industry through first-hand team experiences. While the tech stack has evolved to favor web development, this is just a means to the end.

In focusing on professional software practices, we generally look for the following when choosing the tech stack for the course:

* The underlying languages and frameworks are **modern** and **widely used**.
  
  This generally means that the languages taught here are still prevalent in much of the industry today, and students are likely to encounter it again in the future.

* The underlying languages and frameworks are **open source**.
  
  Generally, software that is open sourced will have robust documentation, which can include Stack Overflow discussions and official bug / issue reports. These can heavily aid students' and staff's ability to debug issues.

* All languages, frameworks, and development tools must be **free to use**.

  All of the tools used in this class must be free to use, at least for this class, without the need to input a credit card. This can include free tiers that cover all class usage, or student / instructor discounts that can be applied to make paid features free (such as the GitHub Student Developer Pack).

* All frameworks should be **testable through a unit testing framework**.

  Through the work of former TA Scott Chow, testing is now an integral part of this course and our mission to introduce students to professional software development practices. Students are encouraged to thoroughly unit test any code they write so the codebase be more easily maintained by future iterations of the course.
