---
layout: essay
type: essay
title: Project Management - the most important aspect of development
# All dates must be YYYY-MM-DD format!
date: 2021-12-17
labels:
  - Software Engineering
  - Agile Project Management
  - Continuous Integration

draft: false
---

Over the course of my formal education, I've learned many algorithms, techniques, and details. How to use Git, Vim, or Visual Studio. Functional programming, design patterns, coding standards. All of this is useful, sure, but it's also stuff I picked up myself pretty quickly as soon as I began to dabble in programming. One thing that always proved challenging, however, was learning to work in groups on small projects. My hobby development focused on smaller personal projects, so I naturally approached group projects the same way. We would collaborate on GitHub, make separate branches, and delegate work, but it always became an entangled mess of merge conflicts and bugs. One person would add functionality to a shared part of code, breaking functionality in another part that someone else adds. Essentially, at least one member of the team would have to refactor the entire thing just to get all of the functionality in, and many many times it would be easier to code the whole thing myself than to try and integrate the changes everyone made without breaking anything.

![](../images/methodology-agile.png)

Finally, in the senior year of my Computer Engineering degree, I've been presented with the right tools to manage group projects so our efforts can be organized and combined effectively without constantly working against each other. Those tools were Agile Project Management and Continuous Integration.

Agile Project Management is a term referring to the iterative cycle of Design → Development → Testing. Each time a new feature is added, testing must be conducted to ensure not only that the new feature works, but also that it didn't break existing functionality. Then the design can be modified or reconsidered. GitHub and other code repository hosts have tools for running a comprehensive test script with each change to a repository, making this process automatic and easy to use. Each developer just needs to add a test script to any new feature they add, and it will be automatically validated along with all existing tests. This process of automatic testing is called Continuous Integration.

I was also taught the tools for managing tasks using the GitHub Projects interface.

Image credit: [https://hive.com/blog/what-is-agile-project-management-methodology/](https://hive.com/blog/what-is-agile-project-management-methodology/) (Accessed 12/17/2021)