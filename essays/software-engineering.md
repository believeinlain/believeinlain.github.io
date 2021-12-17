---
layout: essay
type: essay
title: Project Management - the most important aspect of development
# All dates must be YYYY-MM-DD format!
date: 2021-12-17
labels:
  - Software Development
  - Agile Project Management
  - Programming

draft: false
---

Over the course of my formal education, I've learned many algorithms, techniques, and details. How to use Git, Vim, or Visual Studio. Functional programming, design patterns, coding standards. All of this is useful, sure, but it's also stuff I picked up myself pretty quickly as soon as I began to dabble in programming. One thing that always proved challenging, however, was learning to work in groups on small projects. My hobby development focused on smaller personal projects, so I naturally approached group projects the same way. We would collaborate on GitHub, make separate branches, and delegate work, but it always became an entangled mess of merge conflicts and bugs. One person would add functionality to a shared part of code, breaking functionality in another part that someone else adds. Essentially, at least one member of the team would have to refactor the entire thing just to get all of the functionality in, and **most of the time it would be easier to code the whole thing myself than to try and integrate the changes everyone made without breaking anything.**

![](../images/methodology-agile.png)

## Agile Project Management

Finally, in the senior year of my Computer Engineering degree, I've been presented with the right tools to manage group projects so our efforts can be organized and combined effectively without constantly working against each other. Those tools were Agile Project Management and continuous integration.

**Agile Project Management** is a term referring to the iterative cycle of Design → Development → Testing. Each time a new feature is added, testing must be conducted to ensure not only that the new feature works, but also that it didn't break existing functionality. Then the design can be modified or reconsidered. GitHub and other code repository hosts have tools for running a comprehensive test script with each change to a repository, making this process automatic and easy to use. Each developer just needs to add a test script to any new feature they add, and it will be automatically validated along with all existing tests. This process of automatic testing is called continuous integration.

I was also taught the tools for managing tasks using the GitHub Projects interface. This makes it easy to delegate smaller features to others, and keep track of their progress, and also to communicate to the team which features I'm working on. These tools have proved invaluable, and make me excited to lead teams in the future, in the larger hobby projects I may be able to take on, and in my career as a Software Developer.

## Design Patterns

One final note about design patterns. I find it interesting how much of this field is about familiarity with technical jargon. For example, I was discussing the software design for a robotics team with another programmer and he was asking me about particular design patterns and which I thought would be best to use. I wasn't really able to talk about it because while I had learned, used, and understood various design patterns, I didn't really have the vocabulary to name or discuss them. I ended up advocating for the Publisher-Subscriber design pattern without even realizing it. When I finally was taught about design patterns, I realized none of them were new to me, but if you had asked me if I knew them before, I would have answered you with a blank stare. So I guess **it's as important sometimes to know how to talk about what you're doing as it is to know what you're doing and how to do it.** 

And maybe interviewers can try to remember that talent isn't always communicated well, as some of the best programmers and engineers I know interview terribly. It can be frustrating the extent to which people take "soft skills" for granted, when for some those can be far more difficult to learn than technical skills, and less important. I wonder how many excellent programmers are overlooked because they have difficulty communicating in "normal" ways.

Image credit: [https://hive.com/blog/what-is-agile-project-management-methodology/](https://hive.com/blog/what-is-agile-project-management-methodology/) (Accessed 12/17/2021)