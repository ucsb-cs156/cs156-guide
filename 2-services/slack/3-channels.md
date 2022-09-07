---
layout: default
title: "Slack Channel Layout"
nav_order: 3
parent: Slack
grand_parent: Services
---

# Slack Channel Layout

Throughout the quarter, a number of channels will be created to facilitate the work that the students and staff will be doing in the course. This page lists all channels, provides a brief description of each channel's purpose, and provides instructions on when to create, who to invite, and how to use each one. 

Some things to note:

* Channels here are listed in alphabetical order, like in Slack.
* Channels prefixed with "#" are **public**.
* Channels prefixed with "🔒" are **private**.

## Team channels: #[quartercode]-[section]-[team]

where:

* `[quartercode]` is the short form quarter code for this iteration of the class in lowercase (e.g. "s22" for Spring 2022)
* `[section]` is the time of the section the team belongs to (e.g. "4pm")
* `[team]` is the team number within the section (e.g. 1)

An example of a full channel name is #s22-4pm-1. This also doubles as the official team name in many other places, such as GitHub, GauchoSpace, and the website.

Team channels serve as the main place for team members to communicate and coordinate with each other, starting from the first day of the class. In the beginning phases of the class, much of the interaction within team channels will be guided by assignments and/or suggestions by the staff, with the hope that teams will eventually start to develop the initiative to collaborate on their own, especially as the class approaches the legacy code phase of the course. 

It's worth noting that although this is a team channel, the channels are still *public* within the workspace. This allows for team-to-team collaborations in the legacy code phase of the course, where multiple teams develop for the same codebase. This also allows for any staff member to join in at any time to help a student, so teams are not restricted to only their team's designated mentor(s). Staff are welcome to have team channels for which they are not directly mentoring "muted" to reduce unnecessary pings.

Team channels are also made public so they will be available for export using Slack's export tool on the Free tier. This can be used to retrieve old messages after they are made unavailable through Slack's 10k (and soon to be 90-day) message limit, as well as used for research purposes with informed consent.

Team channels should be created as soon as teams are finalized using the CATME survey data, as they are needed for lecture activities on the first day. As of now, team channels must be manually created by members of the staff, though a process to automate this is reportedly in the works in the UCSB CS GitHub Linker tool.

## #announcements

This channel **must** be the first channel created in the workspace. Every member will automatically be added to this channel, and no one can leave this channel. Additionally, posting permissions should be restricted such that only workspace admins can post. See [Initial Setup](./2-initial-setup.md#the-general-and-announcements-channels) for instructions on setting this up.

This channel serves as a central location for members of the course staff to provide announcements to the whole class. These announcements can include (but are not limited to):

* notices about upcoming assignments and their deadlines
* links to lecture material (e.g. course website, GitHub repos, GauchoCast videos)
* links to / reminders about course surveys (e.g. CATME, ESCI, research)
* tips and clarifications for assignments and the legacy code project
* updates about office hours and staff availability

Since this is the one channel that everyone is a part of, it is also helpful to make use of the channel bookmarks feature to pin the following links for easy access:

* Lecture / Discussion Zoom
* Office Hours Zoom
* CS 156 Course Website
* CS 156 Office Hours calendar

It's worth noting that, although students don't have direct posting permissions, students should still have the ability to start threads from posts in the channel, as well as react to messages. This allows students to ask questions and/or provide feedback on announcements made by the staff.

## #articles

This channel is a place for members to share any interesting articles pertaining to the course / tech stack that they may find. This can include things like release notes for one of the frameworks used in the class, tips on how to better complete a given task, supplementary tools to aid development, and more.

This channel should ideally be created at workspace creation time.

Students are welcome to discover this channel on their own and add themselves if they wish to keep updated. It can be helpful to let students know of the channel's existence near the beginning of the team project phase of the course.

## #bots

This channel serves as a place for Anacapa Slack Bot (and any other bots you may have) to provide their updates, if they have any. It may go unused throughout the quarter - it exists since Ancapa Slack Bot requires a channel to post in for the bot to work.

This channel **must** be created at workspace creation time.

## #general

This channel serves as a place for general, un-categorized discussions to take place. Students can use this as a place to share tips they find and ask general questions about the class (that don't fit in any of the other help channels).

This channel should ideally be created at workspace creation time, and set as one of the default channels that students will automatically be added to upon joining the workspace.

## #help-codecov

This channel serves as a place for students to request to have their Codecov accounts activated within the GitHub organization. Staff members can additionally use reactions to keep track of in progress / completed requests.

The first usage of Codecov is in jpa01, which introduces unit testing, code coverage, and mutation to students. As part of the assignment, students are asked to post a message in this channel with their GitHub username to get their accounts activated.

See the Codecov section for instructions on activating student accounts and what to look for.

When a request is finished, it is helpful to react to the message with a check (✔) to indicate to the student and other staff members that the message has been looked at.

This channel should be created before the start of the jpa01 assignment.

## #help-hwk

This channel serves as a place for students to ask questions about any of the Gradescope homework assignments, similar to Piazza in other classes. Staff and other students can respond in threads.

Note that since the channel is public, potential answers should NOT be discussed in this channel. If a student has a specific case, advise them to start a DM instead. 

This channel should ideally be created at workspace creation time. Since this will be many students' first help channel, it may be helpful to add all students directly into this channel. Additionally, all staff should be added to this channel as members, so they can receive notifications whenever a student posts.

## #help-[assignmentname]

where `[assignmentname]` is the name of a programming assignment, such as jpa01 and team01.

These channels serve as a place for students to ask questions specific to a programming assignment. This will mostly be used for clarifications of assignment instructions and assigned issues, but can also be used by students to ask about submission instructions and deadlines, for example.

These channels should be created as each assignment is released, and staff should be added to this channel at creation time so they can receive notifications whenever a student posts.

While you can add all students directly into the channel, it is easier to instead post a message in #announcements informing people that the channel exists and that they should join. 

## #help-lecture-discussion

This channel serves as a help queue during lectures and discussions, allowing students to request help from a staff member during in-class work sessions. Students place a brief description of their help request in a message, and staff respond to requests in the order the messages come in.

As the operation of this channel is fairly long, it has been factored out into its own document [here](./4-help-lecture-discussion.md).

This channel should be created at workspace creation time, and both students and staff should be added into this channel by default.

## #help-setup-linux-wsl

This channel serves as a place for Linux and Windows WSL users to ask questions about installing and setting up their development tools in these environments. This channel will mostly be used in the first few weeks of the course where many students will be installing these tools on their own machines for the first time. 

It is worth noting that, while the channel name implies that all Linux distributions will be supported, the course website only provides instructions for Ubuntu (as that is what WSL uses by default).

This channel should be created at workspace creation time. In the first lecture (or via #announcements), students should be informed that the #help-setup channels exist and join the channel that corresponds to their operating system. Staff members who use Linux or WSL should also add themselves and answer any questions that students have.

## #help-setup-macos

Like the above channel, this channel serves as a place for macOS users to ask questions about setting up development tools on their macOS machines. This channel will mostly be used in the first few weeks of the course where many students will be installing these tools on their own machines for the first time. 

This channel should be created at workspace creation time. In the first lecture (or via #announcements), students should be informed that the #help-setup channels exist and join the channel that corresponds to their operating system. Staff members who use macOS should also add themselves and answer any questions that students have.

## #ltd-4-x channels

These channels are designed to supplement the [Early Career Software Developers in-class discussion](../../6-in-class-activities/1-early-career-software-developers.md#lecture-2-discussion-of-the-paper). As part of the in-class activity, students will convene in groups corresponding to the section of the paper that they read and analyzed, and the Slack channel will be used to scribe any outcomes and takeaways of the discussion.

The six LTD channels are:

* #ltd-4-1-what
* #ltd-4-2-when
* #ltd-4-3-who
* #ltd-4-4-why
* #ltd-4-5-how
* #ltd-4-6-how-big

These channels should be created before the start of the discussion lecture for the Early Career Software Developers lecture, and will only be contributed to during that lecture. Students will add themselves into the group based on the section of the paper they chose to read. The channel itself will persist in the Slack workspace, and students will be able to refer back to it later on as a way of evaluating their individual and team learning goals for this course (so as long as Slack's message limit doesn't push it away).

## #proj-[projectname]

where`[projectname]` is the name of a legacy code project, such as "courses" and "happycows".

These channels serve as a place for students to ask questions specific to their legacy code project in the legacy code phase of the course. These can consist of questions pertaining to the current or desired functionality of the app or its architecture / design, clarifications about snippets of code, clarifications of assigned issues or epics, for example. It is also a helpful place for staff members to post announcements regarding a specific legacy code project, especially if there are major code changes that were made. 

These channels should be created before students are introduced to the legacy code projects for the first time, whether that's when they start to work on the code directly or through some other activity (such as a Product Management / Product Ownership exercise). Students will be able to add themselves into the channel as long as it's public.

## #random

This default channel serves as a place for anyone to post anything unrelated to the course / department. These can be memes, unrelated articles, YouTube videos, or anything else that others might find interesting or hilarious :)

It's mostly for memes though.

This channel is automatically created by Slack when the workspace is established, and should already be set as a default channel.

## #section-swaps

This channel serves as a place for students to request section swaps before teams are officially formed using the CATME tool (before the first class lecture). After students are initially invited to the Slack workspace through the automatic GauchoSpace email, students who would like to have their section time changed should provide their current and desired sections in a message. If another student has the exact opposite request, a swap can occur, and the instructor should start a group DM with both parties to confirm and officiate the change in GOLD.

This channel should be established at workspace creation time, and will only be used up until teams are finalized. Students should add this channel on their own so others will not be unnecessarily notified of section changes.

## 🔒staff

This private channel serves as a place for general staff communication. All staff communication that does not pertain to grading or legacy code project preparation should be discussed here, including (but not limited to):

* Discussions about upcoming lecture activities and assignments
* Coordination of #help-lecture-discussion, office hours and staff meetings
* Requests for code reviews within the staff
* General course planning and retrospectives

This channel, along with all the other staff channels, should be established at workspace creation time, and all staff should be added to this channel.

## 🔒staff-grading

This private channel serves as a place for staff to coordinate all grading efforts, specifically to ensure that no two staff members are grading the same individuals / teams at the same time. For a given assignment, if grading is not distributed to staff members based on assigned teams, it can help for staff to post which teams they are working on at any given time.

This channel, along with all the other staff channels, should be established at workspace creation time, and all staff should be added to this channel.

## 🔒staff-proj-[projectname]

where `[projectname]` is the name of a legacy code project, such as "courses" and "happycows".

This private channel serves as a place for staff to discuss preparation work for each legacy code project before it is released to the students. This includes epic planning, issue grooming, and development work (such as large refactorings) that need to be done before students can start work. It can be helpful to invite former staff to weigh in on conversations in these channels (as long as no work is assigned).

This channel, along with all the other staff channels, should be established at workspace creation time, and all staff should be added to this channel. (Staff can mute a project channel if they are not directly responsible for the given project)

## 🔒staff-timecards

This private channel serves as a place for Undergraduate Learning Assistants (ULAs) who are paid hourly to request that their timecards be approved by their supervisor (i.e. the instructor of record) after inputting hours at the end of each bi-weekly pay period. The ULA must approve their timecards before it is sent to the instructor, who approves and sends it to the department for final approval.

This channel, along with all the other staff channels, should be established at workspace creation time. However, only the instructor of record and any hourly-paid ULAs should be added to this channel.
