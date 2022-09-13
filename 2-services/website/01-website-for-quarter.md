---
layout: default
title: "Website for Quarter"
nav_order: 1
parent: "Website"
grand_parent: Services
---

Websites for individual quarters are located in the GitHub organization [`ucsb-cs156`](https://github.com/ucsb-cs156) and have names that
match the name of the quarter, e.g. `f22`, `w21`, etc.

They are served via GitHub Pages at urls such as:

* <https://ucsb-cs156.github.io/f22>
* <https://ucsb-cs156.github.io/w21>
* etc.

# Setting up a new repo for a quarter

1. Create the new repo
2. Import the code from the most recent quarter
3. Edit `_config.yml` to set the name of the quarter, and to adjust the dates on the calendar
4. Edit `_data/navigation.yml` to add a new navigation block
5. Copy the `_data/navigation.yml` to the previous quarter
6. Add `current: false` to the previous quarter's `_data/navigation.yml`; this is what produces the banner that says: "Warning: This page is not for the current quarter!"


