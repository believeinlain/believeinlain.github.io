---
layout: essay
type: essay
title: Design - The Foundation of Programming
# All dates must be YYYY-MM-DD format!
date: 2021-12-02
labels:
  - Software Development
  - Programming
  - Design
draft: true
---

### Most people seem to think of programming as a task of simply finding the right instructions to accomplish what they need to do. 
Looking at the vast majority of questions on StackOverflow and tutorials posted to various blogs, one might think that's all there is. "How do I do X with the given language or platform?" These question focus minutely on the details of writing code, but speaking as an amateur programmer for several years before I had any formal education, I would say it's easy to get lost in the woods without taking a single mistep; if you aren't able to abstract, structure, and organize functionality in effective ways.

<img src="../images/boundary.jpg" style="width: 100%">

How many countless hours did I waste correcting the same bug dozens of times because I didn't know how to avoid code duplication? Global variables and mismanaged state led to ephemeral bugs that seemed to go away on their own, only to return much worse later on.

Eventually, over time I developed my own design patterns.

## Antipatterns

Not every design I came up with was a trap. Since C++ was one of the first languages I learned, I understood the importance of encapsulation and abstraction - and since I had worked with BASIC before that I understood how dangerous global variables can be. But I had to find some way to make things come together. Usually I found myself leaning too hard into the things C++ does well, such as class inheritance and templates, resulting in a bulk of structural code without much substance.

## Design

As I was interested in computer game development, I quickly found examples of event-based programming (an example of the observer pattern), as well as many others that I could not necessarily name, but began to understand implicitly. Now the question of programming is one of which pattern to apply in which instance, as I know I'll be able to fill in the details without too much trouble.

Over the years I've found applications for many design patterns. model-view-controller came up when managing server-client interactions in a web app with a database. As mentioned before, the observer pattern is invaluable in interactive real-time applications such as games. Singletons provide a sane way to manage global state, without losing track of global variables, since wrapping them in relevant objects at least allows the way in which they change state together through methods. And finally, using functional programming whenever possible can make even the most convoluted code significantly easier to read and work with. 

I've probably used even more design patterns that I've yet to recognise and identify.
