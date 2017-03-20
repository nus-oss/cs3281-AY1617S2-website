# Contribution to Webpack

## Introduction

Webpack is a module bundler/loader for Javascript and other things. It does a wonderfully lot of stuff, thus leading to its wide adoption in the community.

## Workflow

Webpack moves really fast, which might be a prime example of a project following agile. Webpack first got noticed in 2014, and by the time I'm writing this, Webpack has already released Webpack 2 and has already been working on Webpack 3 in the meanwhile. Every week, hundreds of issues appear, and dozens of pull requests come in.

The workflow is surprisingly simple. Anyone may open an issue and suggest a change or feature that they may want to be implemented, and they can submit a pull request to do so too. The only requirement - any pull request must have an accompanying test. Alghouth large issues may be held back for discussion, but bug fixes are merged almost without question.

It is thanks to the extensive testing that webpack can sustain its pace. It runs on both CircleCI and TravisCI, continuous integration platforms where tests and code coverage and reported for every pull request. It may seem weird that they're using two, but CircleCI provides features that TravisCI does not provide, such as conditionally failable test suite and environments. This allows the version 3 code to conditionally fail, so that maintainers can carry out large refactorings without having to submit a passing pull request every time.

Since Webpack is huge, with a large user base, it is no doubt that Webpack gets hundreds of questions every day. For Webpack 1, documentation was rather poor and thus Webpack 2 has much better documentation. In addition, to mitigate users opening issues to ask questions, Webpack uses Gitter, a chat platform for developers, where people can ask questions and help out each other. Gitter chat receives hundreds of messages a day.

In order to help out with testing, Webpack has a [README file](https://github.com/webpack/blob/master/test/README.md) in the test folder to welcome contributers. The README is very beginner friendly, encouraging and explains the entire structure of the test suite. It is a good example of how to write a README file.

## What I learnt

Moving fast is important, and popularity is immensely helpful for an open source project. It is not useful to anyone if no one adopts the tool (due to risk of it being abandoned) even if the code is extremely well written. Webpack got popular from having an extensive amount of plugins that the maintainers happily accepted in the beginning of the project. Now, thanks to its popularity and the huge amount of contributers, Webpack can successfully improve its code quality and quantity incrementally. This is immediately obvious if you looked at the commit history of Webpack, where the initial code had no comments or documentation.
