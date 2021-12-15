---
layout: essay
type: essay
title: Standard practice - the intersection of style and substance
# All dates must be YYYY-MM-DD format!
date: 2021-09-23
labels:
  - Programming
  - Algorithms
---

## In the interest of clarity

intheearlydaysofwritten
languagetherewerent
conventionssuchas spaces and capitalization

These practices don't carry meaning in themselves, and in fact many languages still don't use them. They developed in English and other written languages because they facilitate communication. Sentences are easier to read when punctuated in such a way. Punctuation itself developed with a similar purpose, although it can also clarify or completely change the tone and meaning of a phrase.

Code is different from the written word in that it carries with it an exact specification for action, which is executed by the compiler or interpreter for that language. In that way, code can be understood as a direct communication from a human to a computer. An intimate conversation. No need for clarification.

Take the C language function below:
```c
int fib(unsigned int n) {return !n?0:n>1?fib(n-2)+fib(n-1):1;}
```
A simple recursive function that computes the `n`th fibonnaci number. Completely trivial for a C compiler to understand, but painful for a human to read and comprehend. We could rewrite this function 100 different ways and they would all yield the same result. But code is not just for computers.

To make the function more clear, we could rewrite it so:
```c
int fib(unsigned int n) {
    if (n == 0) return 0;
    else if (n == 1) return 1;
    else return fib(n - 2) + fib(n - 1);
}
```

This sort of human oriented coding practice makes it easier to pick up a piece of code written by another person and understand what each part does. Modern IDEs have automatic code formatting tools that will rewrite code to be more easily parsed by human eyes.

## More than just readability

"Coding standards" however, represent more than just readability. Project structure conventions and the use of standard library functions or global variables represent decisions that need to be made across a project. Switching paradigms when switching between files can lead to serious bugs, especially when new features are added.

This is why when a company or community develops standards for coding practice that encompass best practices (such as avoiding the use of global variables or the `goto` statement) as well as style choices (such_as_using_snake_case). Linting tools for interpreted languages such as PyLance for Python and ESLint for JavaScript often suggest better approaches along these lines, usually making code more robust as well as more readable.
