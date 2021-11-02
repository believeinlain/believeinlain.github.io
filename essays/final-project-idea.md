---
layout: essay
type: essay
title: "Final Project Idea: Classdoor"
date: 2021-11-02
labels:
  - Software Engineering
  - Meteor
---

# Project: Classdoor
## Overview
*The problem:* It is hard to find information and resources about a specific class if you don’t know someone who has already taken it. Rate my professor requires you to find the professor that taught it before, and radgrad is only for ICS classes.  

*The solution:* A website that allows students to find a class by name (ex - ICS 314), and then either post a review or look at what other students have written about it. Students can also post/view resources that other students thought were helpful in that class (ex-videos, online textbooks, etc.).

## Approach
The website automatically pulls information from the UH course catalog and creates database entries for each course.

Roles: The system should have different roles for each use case. System administrators should be able to edit course information and delete reviews, with the option to block users from posting further reviews. Users should be able to browse courses and write reviews. If a user is blocked, they can still browse and read reviews and resources, but will no longer be able to post.

Possible mockup pages include:
- Landing page (Either log in or start searching for reviews here)
- User home page
- Admin home page
- View reports page
- View class page
- Review writing page
- Review editing page

## Use case ideas
New user goes to the landing page and registers an account. New accounts are only accepted for @hawaii.edu email addresses. Users input their information such as UHM start date, expected graduation date, major, etc. 

User goes to landing page, logs in, and can either post reviews, edit their past reviews, or view other reviews, and report unhelpful reviews.

Admin goes to landing page, logs in, and can view reports on bad users/reviews, and have the option to block/delete them.

## Beyond the basics
- Integration with Star GPS: Users can read reviews on classes they’ve taken or are planning to take based on their Star GPS class schedule and favorites.
- Further verification that a user has actually taken the class they are reviewing.
- Expand so that other campuses can use it too, with a different page for each participating campus (kind of like early Facebook).
- Search courses based on the short hand (ICS 314), CRN, credit hours, 
- Advanced search (similar to Star GPS, filter by prereqs, WI, OC, etc.)

Proposed by Scott Vore, Stephanie Aelmore, and Victor Ho.