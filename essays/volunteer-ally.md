---
layout: essay
type: essay
title: Project Management for Full Stack Web App Development
# All dates must be YYYY-MM-DD format!
date: 2022-05-12
labels:
  - Software Development
  - Meteor
  - React
  - JavaScript
---

For Software Engineering II (ICS 414) at the University of Hawaii at Manoa, I joined a group of five other students to develop a Meteor-based web app for the organization [Volunteer Ally](http://volunteerally.com) based in Hawaii. Volunteer Ally matches volunteers with nonprofits and organizations with a presence here in Hawaii, serving a similar function to websites such as [VolunteerMatch](https://www.volunteermatch.org). The minimum viable product we were to deliver was a site where organizations could log in and post volunteer opportunites, which could be viewed by prospective and active volunteers. Volunteers could then create an account, contact the organization, and register for specific opportunities and track their completed hours on the site. We started with the Information and Computer Sciences department's [Meteor/React template](https://ics-software-engineering.github.io/matrp/) and built the application on [GitHub](https://github.com/ohana-volunteers/ohana-volunteers) using JavaScript. Over the course of the semester I gained some valuable experience, and I'll be sharing what I learned in this essay.

## Client Specifications

Since this was my first experience developing software for a client, one of the first lessons I learned was how their needs and expectations evolve over time. They initially provided us with a simple WordPress blog that emulated the base functionality they wanted to see. This template provided a skeleton for the layout and some basic graphics to get us started. Their initial expectations were lofty, hoping for gamification on top of the base functionality. However, with each client meeting, as they saw more of the site in action, they began specifying new and different details, changing the overall trajectory of the project. **In retrospect, it would have been pragmatic to write a complete design document at the outset and walk through it with a client to glean feedback before we began implementation.**

<img align="center" src="../images/screenshot-volunteerally.org-2022.05.12-21_51_29.png" style="width: 100%">  
Screenshot of the client wordpress site.

## Project Management

Team management for this project was anarchic, which is an approach I wanted to try, but I do not believe it yielded the best results in this case. With no clear delegation of roles or responsibilities, and no clear picture of how the finished product was going to look and function, we each set out to implement different parts of the application using different approaches that did not always work well together. An example of this is one student implementing Volunteer profiles as an extension of the User profile provided in the template, while I implemented the Organization profiles as a distinct collection that can exist separate from any users. Much of the boilerplate in the template did not seem particularly well-suited to our application and was not fully fleshed out, so integrating with it caused more bugs down the line than would have creating our own account and profile structure. Regardless of which decision was wiser, the fact that two of us went down different design trajectories was detrimental to our progress. **It would have been advantageous to assign a "technical lead" role to one of the members, to make broad design decisions and review the code written by other members.**

## Code Reviews

Early on in the semester, we were assigned formal code reviews, where we were tasked with selecting two files in the project, and each member would review the style of the code against provided review guidelines. Early in development, there was not substantial code to review, so the exercise was not fruitful. Code reviews would have been more useful later on, and would have been even more useful if every new pull request was reviewed before merging with the main branch - maybe not every member reviewing every feature, but at least **every feature should be reviewed by someone.** If we had assigned a tech lead, code reviews would have been a suitable task for them.

## Testing

With no strict enforcement of testing every new feature, most code was added and not thoroughly tested at any point. Although I had properly set up continuous integration, tests specific to collections and pages were often not implemented, or at least not implemented fully. This led to the typical issues often seen in larger projects, where the addition of code in one part of the application breaks something somewhere else that no one is aware of at the time, leading to more time wasted chasing bugs. I did learn a lot more about how collections work by implementing tests, so **it would be good practice for each new feature to be testable by continuous integration before a pull request is initiated.**

## Conclusion

In conclusion, while we were able to achieve a minimum viable product in the allotted time, we could have gone further if we had better organization and team management. We should have developed a comprehensive design document to get customer feedback early, assigned a tech lead to make architecture decisions and perform code reviews, performed more code reviews later in development, and tested every new feature before merging it into the main branch. If we had taken those extra steps, then I believe we would have not only have met, but exceeded the client's expectations. 

The finished project is deployed [here](https://volunteerally.connectiveunconscious.com/#/) on a subdomain of my personal site.

<br/>
<br/>
