---
layout: default
title: "Anacapa Slack Bot"
nav_order: 5
parent: Slack
grand_parent: Services
---

# Anacapa Slack Bot

The Anacapa Slack Bot is an in-house Slack application developed as part of the UCSB CS GitHub Linker tool. While the Slack bot is mostly intended to be an admin / instructor tool for analyzing Slack activity, every member of the class can benefit from the "/whois" command, which can be used to identify a student's team and GitHub username.

## Installation

The Anacapa Slack Bot is installed via a button in the github-linker app.  Just click the **Add to Slack** button, as illustrated below

<img width="1061" alt="image" src="https://user-images.githubusercontent.com/1119017/189503488-c5b1129f-fbb2-4904-9b0b-0d3296f81b3d.png">

You may need to actually open up the various drop down menus to review the permissions on the screens that pop up to review them.

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
