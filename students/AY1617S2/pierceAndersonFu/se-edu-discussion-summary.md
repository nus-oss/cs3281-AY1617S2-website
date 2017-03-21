# Summary notes

Discussion held on Monday, 20th March 2017

Topic: Improvements that can be made to se-edu, based on experiences with external OSS

## Tan Wang Leng

#### Worked on
Electron

#### Suggestion
1. Rather than splitting epic PRs into smaller ones that are individually merged to master over time, smaller PRs could be instead closed and later combined into a single epic PR which is then merged to master. This allows one-time migrations when making large system changes.

#### Counterpoints to suggestion
1. Long running feature branches can become hard to integrate over time. Greater divergence from master leads to more merge conflicts down the road.

#### Alternative suggestion
1. Can explore feature flags instead, where features can be merged into master, but not enabled yet.

## Huang Chao

#### Worked on
Zulip

#### Suggestions
1. Development environments can be easily standardized with the use of portable virtual development environments (e.g. using Vagrant). New contributors are less likely to run into issues arising from different development environment setups, making it easier for them to contribute, and reduces the need for others to help debug such issues.
2. Documentation is hosted on readthedocs.org, which supports Sphinx docs written with reStructuredText, and can pull from Git repositories. It supports useful features such as searching and version management. It's also easier to navigate, and looks better.

#### Counterpoints to suggestions
1. Not as applicable to se-edu as our development environment is relatively straightforward.
2. Text would be structured, and it would add a Python dependency.

#### Alternative suggestions
1. Can be applied to TEAMMATES instead as their development environment is more complex.
2. Can look into GitBook as an alternative.

## Jeremy Goh

#### Worked on
phpMyAdmin and TinkersConstruct

#### Suggestions
1. Workflow documents and contributing guides for incoming developers should be clear and easy to find. Learning the code base of a massive, mature OSS is a daunting task, and it can be made to appear more manageable if the right information is made readily accessible to new contributors. Despite our strict standards and extensive guidelines, they are not easily found (oss-generic), and we do not have a workflow guide for new contributors.
2. Templates can be used to create checklists in PR message bodies. For new contributors, the checklist can include reminders to first read our contributing guides, to refer to our convention and guidelines, and to make use of CanIHasReview when the PR is ready for reviewing.

#### Counterpoints to suggestion
2. In the future, CanIHasReview will automatically post in newly created PRs, telling users to submit iterations through it when the PR is ready for review.

## Pierce Fu

#### Worked on
coala

#### Suggestions
1. An improved guide for new contributors, with step based instructions to ease newcomers into our workflow would make our project more approachable, and senior contributors would have to spend less time dealing with common issues. Currently, our guidelines and conventions are detailed, but hard to navigate and aren't broken down into easy to follow steps.
2. Enhancement proposals can be used to keep new and senior developers aware of where we are at as a whole, and what we're working towards at any given point of time. Major changes can be proposed in these documents, and the history of major design changes can be readily referenced through the older enhancement proposals.
3. A public chatroom for newcomers could provide them an avenue to address any concerns or ask for help without cluttering PR threads. Common frustrations by new contributors can also be gleamed from interactions on it, which can then be addressed in the newcomers' guide.

## Chua Ka Yi

#### Worked on
SymPy

#### Suggestion
1. Documentation should be easy to navigate. Do not mix how-to guides with conventions. Documentation for development workflow should be layered to cater to developers with different amounts of experience.
2. Good API documentations should include examples and tests.
3. PR templates can be used to remind developers on the PR title convention.
