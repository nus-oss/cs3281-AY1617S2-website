## Observations: phpMyAdmin and TinkersConstruct

These two projects don't differ in size and maturity - both have a huge user base and huge code base. However,
phpMyAdmin is professionally managed by a team of experienced software engineers while the other is managed by hobbyist
programmers maintaining a popular game modification that the original author had long lost interest in maintaining.

### General work flow of both projects

On the first glance, phpMyAdmin  does not have a very good link to its work flow from its main read me file. My personal
experience starting out in the project is that I had to find the contributing file and any other relevant documents
in repository and the wiki to learn about their work flow. 

Regardless there are some documents they have about their work flow as follows:

* [Contributing.md](https://github.com/phpmyadmin/phpmyadmin/blob/master/CONTRIBUTING.md)
* [Pull Request checklist](https://github.com/phpmyadmin/phpmyadmin/blob/master/.github/PULL_REQUEST_TEMPLATE.md)
* [Release Targets](https://github.com/phpmyadmin/phpmyadmin/wiki/Release_Targets)

Other documents such as setting up are found on their website after navigating some links:
   
* [Setting up](https://docs.phpmyadmin.net/en/latest/setup.html#installing-from-git)

Indeed, starting out in phpMyAdmin is quite a learning experience some information is not immediately available to
you from the main read me file.

In contrast, TinkersConstruct contains all information needed to set-up its development environment in the main
read me file itself. It should be noted that the setting up of development workspace is made very simple due to
the massive amounts of `gradle` scripts developed by the main game modification API which this software is based
upon. There a two documents about the general work flow of this project, and it is as follows:
    
* [Contributing.md](https://github.com/SlimeKnights/TinkersConstruct/blob/master/CONTRIBUTING.md)
* [Readme.md](https://github.com/SlimeKnights/TinkersConstruct/blob/master/README.md)

It is interesting to note that both projects do not have any links nor documents about coding standards. It is probably
safe to assume that both projects adopt the "just follow the style in the file" coding standard which is to make sure
all your code's syntax matches the syntax of the rest of the code.

### Learning points from contributing to two contrasting projects

Contributing to a project that is professionally managed and one that is not is really an eye-opener and it shows that
mature OSS projects are not necessarily managed by a team of professionals. The following are points I have learned
when I contributed to both projects:

* A clear guide to help new incoming developers to get started coding in your project is very essential. Learning 
the code base of a massive mature OSS project itself is a daunting task - so it is essential that project maintainers
ensures that the developers can start working on your code base easily.

  * phpMyAdmin in this case is harder to start working with as it requires some searching for the relevant documents to
get started. It uses composer to manage its project dependencies so upon finding the starting out guide, the project set
up is relatively simple and straight forward. 

  * In contrast, TinkersConstruct with the use of multiple `gradle` scripts,
abstracts away the otherwise very complicated set up for its development workspace away from all incoming developers.
Instead it just asks all incoming developers to  run the script in the command line. For reference, the script takes 15
minutes to run and in the process downloads and manages hundreds of dependencies. It even has a set up script for the
Eclipse IDE to create a Eclipse project file so that developers can open the IDE and point to the folder and start
working on it.

* Start working on small issues first. Smaller PRs with very localized changes by new developers will be merged faster.
Try not to be too ambitious with the first few PRs even though you know how to fix a particular issue: your solution
might already been thought of but not already implemented because of reasons that are still not known to you because 
you are new to the project.
  
* Always keep changes to the minimum. Some issues can be easily solved with a one-liner change after studying the code
base a little. These PRs tend to get merged without issue in the first few iterations rather than being rejected or
subjected to a few reviewers requesting the author to find a better solution to a trivial problem that does not involve
changes in multiple files.

* Comply with instructions. In the case of phpMyAdmin, all commits have to be signed off with a real name and email
address in order to signify that you agree that your code submitted will follow their terms in the license. This
signing off of commits is of course new and might cause your PRs to be rejected because of this small detail.

### Suggestions for SE-EDU projects

The practices adopted in SE-EDU projects are actually very advanced in comparison even with professionally managed
projects like phpMyAdmin. Therefore it is imperative that clear links to the project work flow is required. 

For example, SE-EDU can adopt the pull request document adopted by phpMyAdmin. This document will automatically be
inserted in the body of all new pull requests by github and it should contain links to the expected work flow in
creating PRs in SE-EDU. In addition, a checklist can also be inserted in the document give very short list of steps
(with links to the more verbose explanation in OSS-generic) to complete before submitting a PR to SE-EDU.This will
eliminate the initial confusion of adopting a very advanced high quality work flow that is different from many other
OSS projects.
