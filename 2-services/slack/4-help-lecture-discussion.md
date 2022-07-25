# #help-lecture-discussion

Originally established in Fall 2020 by Andrew as a way to combat the large number of "Ask for Help" requests on Zoom that were only visible to the meeting host, #help-lecture-discussion is a queue for students to request help from staff member(s) during formal instruction periods. 

Through the queue system that we have established, students can not only request help, but also practice the process of asking questions formally in an industry setting, especially in large organizations where the people whom you seek help from may not be physically present.

## What does a help request look like?

A help request, at minimum, should include the following items:

* A short description of the issue to be resolved
* The location of the student (a table number if in person, or a breakout room name if on Zoom)

As the course progresses into the legacy code phase of the course, if a help request pertains to code / development work, it is helpful to ask students to include the following, similar to an actual issue report:

* Links to any relevant instructions and related issues
* Links to code repositories / snippets and Heroku deployments (if applicable)
* A description of what steps the student / developer has already tried
* Any relevant screenshots (e.g. of error messaging)

## Setting up the channel

Since this channel is used by everyone, it should be created at workspace creation time and set as a default channel for everyone to join. Instructions to do so are located in the [Slack setup guide](./2-initial-setup.md#creating-the-workspace).

## Starting a work period

At the beginning of each work period, it is helpful to remind students of post requirements in #help-lecture-discussion channel through a short message:

> **@channel January 1 Lecture**
> 
> Here's a reminder to place help requests in this channel instead of raising your hand or using the "Ask for Help" button.
> 
> When asking for help, please **give a short description of your request**, and **list your current breakout room or table**.
> 
> Keep help requests to a single message and place any supplementary information in the message thread. Thanks!

This establishes the start of a help queue for a given lecture or section, but this does not mean that staff should immediately start attending to requests. **Staff should not answer any requests until the team is finished with their daily standup**, even if posted before they are finished.

If working in South Hall 1431, it is helpful to have Slack open on the main lectern computer and displayed on the projector and the four TVs mounted on the sides of the room. This allows for staff members to easily glance at the queue and make judgments on how much time to spend with a student.

## Staff: Responding to requests

When a help request is open, a member of the staff can start work on the help request by reacting to it with "👀" (`:eyes:`). This signals to the student and other staff members that **this request is being looked at / attended to** by the reactor.

When a help request is finished, the person completing the request should remove their "👀" react and replace it with "✔" (`:white-check-mark:`). This signals to the student and other staff members that **this request has been completed and the issue is resolved**.

If a staff member is unable to resolve a help request and needs assistance from other staff members to complete the request, they should add a "🆘" (`:sos:`) reaction to the message. This signals to other staff that **this request needs additional help**, and staff should attend to it as soon as they can. Upon resolution, this react should be removed.

Generally, requests should be answered in the order they are posted, unless a request:

* is too vague and needs more clarification (per the guidelines in [What does a help request look like?](#what-does-a-help-request-look-like))
* is posted before the team has finished conducting their daily standup
* requires the help of specific staff members (e.g. those directed toward a specific project)
* comes from a table / team that already has multiple staff members attending to it

## Closing the help queue

In order to give requests sufficient time to be answered (to some degree, even if not fully answered), the help queue should be closed 5-10 minutes before the end of a work period. This prevents students from holding back staff after a lecture or section is over, cutting into unpaid time (which is strictly forbidden by the university).

To close the queue, post a message like this into the channel:

> @here We're going to close the queue here as we are approaching the end of class. Feel free to get help at office hours or at the next lecture!

If the staff notice that the queue is growing abnormally long, which tends to happen near the end of the quarter as students approach the pull request deadline, staff can use their discretion and collectively close the queue early so they have enough time to get through the rest of the queue.

## Future suggestions for #help-lecture-discussion

In the beginning phases of the course, it is okay to be laid back on post requirements - a short description and location is usually enough for the correct staff members to attend to the request. In the interest of saving staff time and encouraging professional communication practices in industry, however, it may be helpful to enforce more detailed requests as the course progresses, eventually getting to the point where help requests won't be considered if they don't include the full issue format.

One way to encourage this would be to have a "message template" similar to an issue template on GitHub:

> To start a help request, copy and paste the following into a single message and answer the questions:
> 
> ```
> *What are you trying to accomplish?*
> *What have you tried so far?*
> *Where are you located? (Table or breakout room)*
> ```
> 
> To further assist the staff, place the following in the thread if applicable after posting your request:
> 
> * Links to repositories / code snippets, issues, and/or Heroku deployments
> * Screenshots / pastes of any relevant error messages

Another way would be to establish a Slack workflow or app to handle such requests. The former feature, Workflows, is only available as a paid feature, but it essentially allows students to fill out a short form within the Slack channel and the form will add messages on the student's behalf. The latter, Slack apps, would have to be custom developed, and could be made available as a slash command.

Additionally, some tooling could be added to the UCSB CS GitHub Linker tool to analyze this channel. Some metrics that could be particularly useful to analyze are:

* number of help requests per person
* number of help requests per team
* relative time between help requests and their associated pull requests
* number of help requests per lecture / section as the course progresses

This could be used to see whether team performance is affected by if, how, and when they ask staff for help. One hypothesis is that teams that request more help progress quicker, but another hypothesis is that teams that tend to be more dependent on the staff for help aren't making full use of the resources available to them, and tend to struggle more, similar to findings in the Begel and Simon analysis of new hires at Microsoft.
