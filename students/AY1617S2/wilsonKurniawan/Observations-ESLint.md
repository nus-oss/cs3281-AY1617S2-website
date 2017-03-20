# Contributing to ESLint

Author: [Wilson Kurniawan](https://github.com/wkurniawan07)

Contribution: [`Build: display rules’ meta data in their docs (fixes #5774)`](https://github.com/eslint/eslint/pull/8127)

## Links to ESLint workflow documentation

- Developer guide
  - [Architecture](http://eslint.org/docs/developer-guide/architecture)
  - [Setting up developer environment](http://eslint.org/docs/developer-guide/development-environment)
  - [Contributing guide](http://eslint.org/docs/developer-guide/contributing/), which includes how to report a bug, propose new features, work on issues, submit PRs.
- [Maintainer guide](http://eslint.org/docs/maintainer-guide/)
  - Includes: how to review PRs, manage the issue tracker, manage releases
  - Also documents the [organizational structure](http://eslint.org/docs/maintainer-guide/governance.html)

## Observations and things to adopt

- [Contributor License Agreement (CLA)](https://www.clahub.com/pages/why_cla)

ESLint requires all its developers to sign a [CLA](https://cla.js.foundation/eslint/eslint), essentially granting the project the permission to use the developer's work.
From the maintainers' point of view, it frees them from possible legal issues arising in the future should the developer suddenly decide to withdraw his/her permission.

**To adopt:** CLA might be something useful (albeit not the highest priority) for TEAMMATES.

- Importance of documentation

ESLint maintains a very well-written and very precise documentation.
They list down even details such as [who and when to merge pull request, or when to close a pull request](http://eslint.org/docs/maintainer-guide/pullrequests.html) and [how to do releases](http://eslint.org/docs/maintainer-guide/releases.html), aside from usual items such as setting up guide, architecture, and contribution guide (links given on the previous section).
They also host their documentation in a Jekyll-powered website, which allows for better organization and capabilities such as searching and navigations.

TEAMMATES also has documentation of arguably similar quality, at least for the usual items. It currently misses a maintainer guide which makes handing over to the next leading team not so trivial (e.g. maintainers are not sure of how to run things).

**To adopt:** (1) a maintainer guide for TEAMMATES (WIP!), (2) a website to host documentation (GitHub pages?).

- People before code

> Build community, not software. Without community your code will solve the wrong problems. It will be abandoned, ignored, and will die. Collect people and give them space to work together. Give them good challenges. Stop writing code yourself.
>
> [*Ten Rules for Open Source Success*](http://hintjens.com/blog:95)

ESLint is the leading linting tool for JavaScript, from the older ES5 standard to the latest ES2017 standard.
Arguably, one of the reason behind its success is the large community: large user base and large developer base.
Despite being a large project with non-trivial difficulty, ESLint has successfully attracted many external contributors (GitHub has recorded that they have received contributions from **486** contributors).

While ESLint has a team of core maintainers (in their own term: Technical Steering Committee/TSC) to decide the direction of the project, they are very welcoming to external contributors. They adopt a [meritocratic governance model](http://oss-watch.ac.uk/resources/meritocraticgovernancemodel) which values a person based on his/her contributions, maintain a very well-written developer and contribution guide, and respond to external contributors very quickly (they have 8 TSC members and as many as 14 committers). It also helps that the developers of ESLint can relate to the application domain very easily, and they know what contributing to ESLint will entail.

What does this mean for TEAMMATES? TEAMMATES arguably adopts the same meritocractic governance model, has an arguably high-quality developer guide, and respond to contributors within 24 hours barring busy period (such as exams). What TEAMMATES lacks is *the purpose of contributing to the project*. Is it to learn Java/JavaScript/...? Is it to make peer evaluations great again? Is it to add an entry of "contributing to an open source software project" in one's resume? Is it something else? The onus is on the contributors themselves to find out why, but when the application domain is quite distanced from them, such a purpose may not be easy to find.

**To adopt:** Why contribute to TEAMMATES?

- Commits and PRs

ESLint requires prefixing commits with [the type of work done](http://eslint.org/docs/developer-guide/contributing/pull-requests#step-2-make-your-changes) and that the commit summary must not exceed 72 characters.
Multiple commits are allowed although I have observed that most issues are resolved via single commits, and the workflow used is rebase-and-merge; that is, all commits from a PR will be stacked on top of the latest `master` branch and there is no merge commit which "pollutes" the commit history.
This makes it very easy when browsing the commit history: the type of work done and the summary is immediately displayed, and additional information is provided if necessary.

TEAMMATES, on the other hand, uses the issue title as the commit message on `master` (using squash-and-merge workflow), and no restriction on the commit messages on branches as long as they are sensible.
Given that the merge commit message *also* includes the link to the issue (on GitHub), the commit message becomes redundant. Essentially, to get a clearer picture on why certain commits are done, one needs to refer to the issue on GitHub. This is not necessarily a bad practice, but it adds an unnecessary dependency to GitHub instead of simply `git log`.

**To adopt:** Commit messages are as important as other forms of code documentation, more so because commit message **do not** get outdated. If the opportunity presents itself, TEAMMATES should move to rebase-and-merge workflow and proper commit message enforcement. This would add another item to the developers' and reviewers' checklist: that the commit messages should adhere to the standard, however it should be worth the trouble in the long run.

- Automation

ESLint automates many of its processes: triaging issues (ensures they follow the provided templates), finding reviewers for PRs (via Mentionbot), checking PRs (ensures correct commit message requirement and signed CLA), continuous integration (Travis CI, AppVeyor CI), and release management, including making changelogs.
This saves the developers and maintainers alike from tasks that are more mundane.

**To adopt:** The only automation that TEAMMATES observes is static analysis and continuous integration via Travis. TEAMMATES could benefit from automation in more fields such as release management, triaging issues, and checking PRs (so far limited only to PR title and `Fixes #....` keyword).

- Versioning and changelog

In ESLint, version numbers are treated very seriously.
Regular releases will only observe an increase in *minor* version, while patches will be included in the same minor version but an increased *patch* version.
An increase in *major* version generally means backward-incompatible changes, e.g. if a feature is removed or an API is changed.
ESLint documents their usage of versioning [here](https://github.com/eslint/eslint#semantic-versioning-policy).

This is not the case for TEAMMATES where version number is a mere "formality".
However, this is not a big problem as TEAMMATES is an end product not meant to be used by developers.
Nevertheless, changelogs will still be helpful to developers and users alike, otherwise they will feel that nothing has changed for the past few versions or so.

**To adopt:** Changelogs; related to the previous section on automation.

- Minimum supervision on developers (particularly IDE)

ESLint does not impose any IDE usage on its development workflow; the only common ground is tasks to be run via command line.
This means developers are free to choose their IDE of choice (or even lack thereof), which undoubtedly make the developers feel more unconstrained.

TEAMMATES, on the other hand, started as an Eclipse-specific project and thus its workflow is highly suited for Eclipse.
Developing with other IDEs such as IntelliJ or Netbeans was impossible in the past (core team members will ask them to switch to Eclipse), which undoubtedly becomes a disincentive to many of them for contributing to TEAMMATES.
This has been alleviated to a large extent through the introduction of Gradle (in 2016) and more recently the experimental support for IntelliJ.

**To adopt:** Granted that IDEs help in many tasks, their usage (especially a particular IDE) should never be a requirement. It places additional overheads for developers (old and new), and additional works for maintainers when support request for IDEs come ([very evident in TEAMMATES](https://github.com/TEAMMATES/teammates/issues?utf8=✓&q=is%3Aissue%20is%3Aclosed%20label%3Aa-DevHelp%20)).

## Suggestion for ESLint

- Decommission the usage of mailing list

ESLint maintains a few communication channels: GitHub, Gitter, Twitter, and Google groups mailing list, however the mailing list is not very active and its contents can be moved either to Gitter or GitHub. It will be favorable (less maintenance burden) for them to decommission their mailing list.
