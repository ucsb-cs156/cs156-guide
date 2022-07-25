# Initial Team Formation

The team formation process starts as soon as students are able to enroll in the course, with the goal of having teams finalized by the first lecture or discussion section. For a typical class of 72 students, we form twelve teams of six students, with four teams in each of the three discussion sections. 

We utilize the [CATME Team Maker](https://info.catme.org/features/team-maker/) tool to assist in forming teams. The Team Maker tool allows instructors to establish a set of survey questions about students, where each question establishes one "criterion". Each criterion will be weighted for similarity / dissimilarity and given a score. CATME will then optimize the possible student team formations, seeking the formation that produces the *highest minimum score* across all teams. 

## Survey Criteria

In CMPSC 156, the actively-used survey criteria used are:

* **Primary Operating System / Platform**

    Unlike in industry, we do not have a consistent and reliable computing environment that students can use to develop. CSIL serves this purpose in many other classes, but due to the complexity of projects in this class (especially since we use Node.js), CSIL's networked file system becomes a heavy bottleneck when developing in this course. As a result, students are encouraged to use their own development machines.

    This question allows students to designate which operating system(s) they have access to and are comfortable using for this course on a daily basis. Students will be grouped with other students using the same platform, with the goal of allowing students to help each other debug in cases of platform-specific issues.

    This criterion has a weight of 3.

* **Gender**

    We do not discriminate based on gender, and we want to avoid putting students in situations where this can occur. In an ideal world, we would want to form teams such that each gender is equally represented in every team, but in reality, there is a large gender disparity in the field of Computer Science which remains unsolved.

    In CATME, gender data is only used to ensure that we do not end up in a scenario where a team member has only one person of a specific gender. For example, given a team size of six, we want to avoid teams that have five male-identifying students and only one female-identifying student.

    This criterion has a weight of 10 due to its high priority.

* **Preferred Working Methods**

    While this question was mostly established for Winter 2022's hybrid return to campus, this question remains relevant due to evolving work-from-home policies in industry, especially in software roles that are able to be performed remotely. This gives teams the opportunity to experience "working" in a remote team.

    This question allows students to select whether they would prefer face-to-face, hybrid, or purely virtual / online instruction. Students will be grouped with other students with the same / similar preferred working method.

    This criterion has a weight of 4 (?).

* **Previous Java Knowledge**

    This questions allows students to rank their previous knowledge of Java on a three-point scale (1-3). Students will be grouped with other students with similar ranking of Java experience. This is done to prevent scenarios where certain team members are highly experienced while others are beginners, as experienced team members tend to "carry the team" and complete all the work instead of helping the beginner students learn.

    This criterion has a weight of 4. 

* **Previous React Knowledge**

    Like the above criterion, this questions allows students to rank their previous knowledge of React on a three-point scale (1-3). Students will be grouped with other students with similar ranking of React experience.

    This criterion has a weight of 5. 

Note that the above criteria weights were interpolated from the final Winter 2022 team formation scores. (This should be verified later by Prof. Conrad.)

Other possible criteria, including ones that were previously used but are no longer in use, are:

* Previous Industry Experience
* Time Zone (for purely online quarters)

In Spring 2022, students were also given the ability to specify desired teammate(s). Such requests were not guaranteed, but were mostly honored. (I'm not sure if these were manually done, or if there was a way in the CATME interface to specify desired team pairings. Prof. Conrad will have to clarify here.)

## Importing Class Rosters into CATME

(I have never used CATME before, both as a student and as course staff, so these instructions may have to be fleshed out a bit more by Prof. Conrad.)

Class rosters can be imported into CATME to start the Team Maker process. Information must be provided in CSV format and contain the following columns:

* First Name (header name `f`)
* Last Name (header name `l`)
* Email (header name `email`)
* Student PERM (header name `id`)
* Enrolled Section (header name `section`)

Note that section swaps, drops, and late adds must be manually handled. 
