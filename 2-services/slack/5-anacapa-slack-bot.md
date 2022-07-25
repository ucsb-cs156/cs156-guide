# Anacapa Slack Bot

The Anacapa Slack Bot is an in-house Slack application developed as part of the UCSB CS GitHub Linker tool. While the Slack bot is mostly intended to be an admin / instructor tool for analyzing Slack activity, every member of the class can benefit from the "/whois" command, which can be used to identify a student's team and GitHub username.

## /whois command

In any Slack channel in the workspace that Anacapa Slack Bot has been added to, you can use the following command:

```
/whois @user
```

where `@user` is a Slack mention of the student whose info you would like to look up. This **must** be a Slack mention - simply inputting a username isn't enough here.

The Anacapa Slack Bot will respond with the following basic information about a student:

```
GitHub ID: andrewhlu, Student: Andrew Lu, Section: 4pm Teams: s22-4pm-1
```

Additionally, a few values have hyperlinks. Specifically:

* The student's GitHub ID has a hyperlink to their GitHub profile
* The student's name has a hyperlink to their student profile in the UCSB CS GitHub Linker tool (usable by instructors / TAs to view information about a student's repository permissions and contributions)
* The team name has a hyperlink to the team in GitHub's teams interface
