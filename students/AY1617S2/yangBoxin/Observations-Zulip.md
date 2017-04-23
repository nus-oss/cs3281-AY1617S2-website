# Contributing to Open Source: Zulip

## Introduction to Zulip

Zulip is an open source group chat application. It is owned by Dropbox and a group of full time employees are maintaining the project. The main technology used in Zulip server is Django framework in Python, together with Tornado for realtime push, PostgreSQL for database and NGINX for linking Restful API with Django url.

## Development environment

Zulip team builds up a Vagrant developerment environment, which runs Zulip development server in a Virtual Machine in Ubuntu. Though demanding significant amount of time to set up, Vagrant ensures that server is running under expected environment with all dependencies installed in the Virtual Machine. Vagrant automatically synchronizes local codes to the Virtual Machine and runs the test.

## Learning process

As Python and Django are new to me, I started learning from scratch from following resources:

1. Introduction to [Python](https://www.python.org/about/gettingstarted/) from official website
2. Video workshop for [Django for Beginners](https://www.youtube.com/watch?v=zTNA0MtZwso)
3. Django [tutorial](https://docs.djangoproject.com/en/1.11/intro/tutorial01/) from official website
4. Zulip specific [tutorial](https://zulip.readthedocs.io/en/latest/) written by zulip developer 

## Special characteristics of Zulip

### Using bot to facilitate tagging of Issue
Zulip developed their own [bot](https://github.com/zulip/zulip/tree/master/bots) to help with the development process. By tagging Zulip bot, external contributors can claim the issue and the issue will be assigned to that developer. Also, by tagging the issue with areas, Zulip bot automatically tag group members in charge of that area. If the issue is claimed but not finished for a long time, the zulip bot tags the assignee for reminder. Basically, Zulip bot does what is similar to Teammates bot, but with more powerful features.

### Encourage Work in Progress discussion
Zulip encourages Pull Request that is work in progress to be pushed and maintainers provide feedback on the current work.
Besides, Zulip opens their a Zulip server for communication between developers. When I was in doubts, I could private message the author of the issue to clarify, and I could post in the public channel such as #development help to ask for help. Usually the responses come very timely.

### Squash and Rebase for a cleaning git commit history

### Run test automatically before trying to commit

## What I learnt from contributing to Zulip

### I do not need to learn everything to work on my Pull Request
Zulip is a big project involving a lot of technology. I started off by learning all the tutorials provided by Zulip and ended up spending a lot of time without pushing any code. For my later PR I learnt from the code base on how Zulip code works and fixed bugs.

### Work from smaller PR
At beginning I started off with a bite size issue, however later as I discussed more with the issue author he realized that it was a much bigger PR and I was stuck for days before I gave up.

## Things we can adopt to Teammates
1. More powerful bot for Issue and PR Assignment and labeling.
2. Using an online discussion group such as Zulip or Gitter to allow developers, especially from external organizations to communicate better with the core team.
3. Allow work in progress to help people who are stuck.
4. Provide more tutorials and learning resources, especially for the technology we used such as JSP Standard Tag Library. Other materials specific to Teammates such as directory structure and walk-through of a big PR might be helpful for new contributors to learn about Teammates codebase
5. Build Vagrant for development and testing. Running Teammates testings on my local Mac always have failing cases and bizzare behaviours. If Vagrant is build, we can enforce running test before trying to push to remote and run it on Travis.
