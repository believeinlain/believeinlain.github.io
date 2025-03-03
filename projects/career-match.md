---
layout: project
type: project
image: images/cm-square.png
title: UH Career Match
permalink: projects/career-match
# All dates must be YYYY-MM-DD format!
date: 2021-12-15
labels:
  - JavaScript
  - Meteor
  - React
  - MongoDB
summary: Web app built in Meteor with React and Semantic UI for connecting companies with UH students via skill and location matching.
draft: false
---

UH Career Match is a web app I developed along with my classmates for ICS 314: Software Engineering I, at UH Manoa. To accomplish this project, we used the [Meteor Framework](https://www.meteor.com) along with [React](https://reactjs.org), [Semantic UI](https://semantic-ui.com), and [MongoDB](https://www.mongodb.com).

<img src="../images/cm-landing.png" width="700">

For project management, we used issue-driven development with Github Projects. I played the role of project manager, identifying tasks to meet our milestone requirements and creating an issue for each one.

<img src="../images/cm-project-management.png" width="700">

The team worked together to implement the functionality needed to address and close each issue. I was responsible for implementing the following issues across the three milestones:
- Deploy app to Digital Ocean
- Update github.io page with links as required
- Redesign page organization for simplicity and ease of use
- Create development database entries to test search function
- Put your system under contiguous integration using GitHub Actions.
- Update your organization’s GitHub Page to document the current version of your system following GitHub hosting guidelines.
- Fix routing for implemented pages
- Implement TestCafe “availability” tests for all pages.
- Display the current results of continuous integration via a badge on your project home page.
- Update career-match.github.io with latest changes to close out module 2
- Refactor to simplify profile/account association and fix bugs for deployment

As evidenced by the issues I closed, I managed deployment and continuous integration, and played a part in application design, database management, and documentation. I also identified and addressed an issue with limited resources on GitHub Actions, as testcafe would consistently fail the first test while the app was loading, even with a 10 or 20 second delay. The solution I found was to add `--page-request-timeout 100000` to the testcafe start script, which ensured the app would wait for 100 seconds before failing on timeout. This eliminated the need to wait for an arbitrary period of time, and reduced delays when sufficient resources are available to start quickly, given that it only waits until the page request is satisfied.

For deployment, we used [Meteor Up](http://meteor-up.com) to deploy our app onto a [DigitalOcean](https://www.digitalocean.com) droplet running [Ubuntu 20.04](https://ubuntu.com). The app is currently hosted at [https://career-match.connectiveunconscious.com](https://career-match.connectiveunconscious.com), sharing the primary domain with my personal site for convenience. This also gave me the opportunity to implement SSL encryption, which was easy to accomplish since Meteor Up automates the entire process.

Since I managed deployment, I also learned live database management, since the command `meteor reset` that works well on local installations doesn't work on a deployed container. Dropping the database through MongoDB with `db.dropDatabase()` didn't always work, as sometimes the admin account would remain, requiring me to drop the database again to allow it to be fully reset. It makes sense that deployment is careful not to disturb the existing database, but that makes changes to database structure challenging to implement in practice. Certainly something to take into consideration for future projects.

Career Match was developed in collaboration with Cathy Kim, Gerald Lee, Ian Eshelman, and Jay Ramos. Read more about the project [here](https://career-match.github.io). Source code for the project can be found [here](https://github.com/career-match).
