# Contributing to freeCodeCamp

## Workflow

freeCodeCamp has quite a complex set up with many dependencies and prerequisites that need to be downloaded before you can begin contributing.

The good thing is that freeCodeCamp provides an extensive document, [Contributing.md](https://github.com/freeCodeCamp/freeCodeCamp/blob/staging/CONTRIBUTING.md), which not only documents how to set up freeCodeCamp on your local machine, but also documents how to use git.

freeCodeCamp also has a [Gitter](https://gitter.im/FreeCodeCamp/Contributors), which is a chat room where contributors can ask questions on anything that they are unsure about. freeCodeCamp has an active and helpful community, which is excellent for beginners who want to contribute.

There are many simple issues in freeCodeCamp, ranging from spell errors in documentation to small bug fixes, which are easy for new contributors to do. The issues are also usually tagged with `help wanted` or `first-timers-only` to help identify them as simple issues for beginners. In addition, the codes in freeCodeCamp are very modular, making it simple to make changes to a certain portion of the codes without needing to understand the overall picture. This makes freeCodeCamp a very good OSS to contribute to for your first PR.

## Learning Points

Contributing to OSS projects is not as daunting as it first seems. Most of the time, the reviewers are friendly and helpful because they want people to contribute to their OSS. 

When doing a PR to an OSS, it helps that your PRs are small and have good description of what you are doing and why you chose to do it that way. Having an explanation can be very helpful to the reviewer, which will end up with more of your PRs being merged faster.

## Practices/Tool that can be adopted

Many OSS projects are daunting for beginners. Compared to [PowerPointLabs](https://github.com/PowerPointLabs/PowerPointLabs), freeCodeCamp makes it easier to contribute by:

* Having a `Gitter` chatroom

Having a `Gitter` chatroom means that any developer, new or existing, can ask questions regarding anything more easily. This makes contributing to the project less daunting, as there is always a platform for any queries. PowerPointLabs does have a contributor's forum. However, the forum is no longer active and also requires a Google account to join, whereas Gitter only requires a Github account, which everyone who wants to Contribute should have.

* Having a `help wanted` label for issues

Having such a label means that new contributors can easily identify easy fixes or issues that require help. This makes finding a suitable issue to do easier, which lowers the entry barrier, especially for beginners. I notice that the label `d.FirstTimers` exists in PowerPointLabs. However, the label is barely used. In this case, the label actually deters new contributors, as they will be unable to find issues that they can contribute to, even when using the label.

* Having a checkbox list for PRs

freeCodeCamp has a checkbox list which appears automatically whenever a PR is made. This helps remind contributors of the different things they have to do before making the PR. This helps beginners and contributors who have no contributed for awhile to remember the process without needing to go through the entire Contributing.md document again.

* Having larger issues

The idea for having small issues is that each PR can reference an issue without needing to be too huge. While this is a good idea, it is sometimes necessary to have larger issues instead of polluting the issue tracker with small issues that fix the same overall problem.

## Suggested areas for improvement

One thing that freeCodeCamp can improve on is their **set up process**. Although they have a very detailed guide on how to set up the project, they can instead put all the dependencies together in a script and allow the user to execute the script to download all dependencies, instead of asking the user to download each one manually.

Another thing that freeCodeCamp can improve on is to **remove their policy to only have 1 commit per PR**. The policy is in place to help keep the commit tree clean. However, it is not necessary, as Github is able to `Squash and Merge` PRs. Having such a policy only makes it harder for reviewers to review the PR, and forces contributors to squash their commits everytime they make a change for the reviewer.