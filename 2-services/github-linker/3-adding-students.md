---
layout: default
title: "Adding Students"
nav_order: 3
parent: github-linker
grand_parent: Services
---

# {{page.title}}

## To add students to the linker

### Prepare the .csv file for upload

1. Download a course roster from <https://egrades.sa.ucsb.edu> and upload it into Google Sheets where you can manipulate it
2. Create a sheet to translate enrollment codes to sections, such as this:
   <img width="366" alt="image" src="https://user-images.githubusercontent.com/1119017/189503769-2bc01b7c-5af5-4f57-81c3-70c0d113a4e3.png">
3. Add a column for sections, with a formula such as this.  (Here, C2 is the column with the Enroll Cd in it.)
   ```
   =vlookup(C2,enrollcode2section!A:B,2,false)
   ```
4. Optional: Convert Last Name and First Name to a more friendly format using `PROPER(E2)`
5. Optional: Convert `@umail.ucsb.edu` addresses with a formula such as: `=substitute(H2,"@umail.ucsb.edu","@ucsb.edu")`

### Upload the CSV file here

<img width="650" alt="image" src="https://user-images.githubusercontent.com/1119017/189503955-a23bbf9b-650c-4170-9d07-3a152e8b5727.png">

## Messaging Students

Here's a sample message:

```
Dear CMPSC 156 Students:

In preparation for our course, I'd like to invite you to join the course GitHub organization.

It's quick and easy; less than 5 minutes of your time.  Here's what to do:

(1) Create a github.com account if you don't already have one; create it on the free plan.    (If you already have one, you do not need to create a new one; it is better to keep all of your GitHub activity under one account.) 

(2) Add your ___@ucsb.edu email to your GitHub account if it is not already there. (Do this under "Settings". You can have multiple emails on your GitHub account.)

(3) Visit https://ucsb-cs-github-linker.herokuapp.com and login with your GitHub account.

(4) Look for the course ucsb-cs156-f22, and click the green "Join" button.

(5) You should see a message with a link to a page on https://github.com where you can accept your invitation

(6) Click to accept the invitation.

That's it!  It will help us get into the interesting stuff faster if we can take care of a lot of these housekeeping tasks before the course starts.

```
