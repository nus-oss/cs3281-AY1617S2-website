# Observations: Electron project

## General Workflow Documentation

* Contributing guide: https://github.com/electron/electron/blob/master/CONTRIBUTING.md
* Build & coding standards: https://github.com/electron/electron/tree/master/docs/development
* FAQ (when will Chrome and Node.js be migrated): https://github.com/electron/electron/blob/master/docs/faq.md

## Learning Points

* Providing clear documentation (related to both the code and the project maintainence workflow) is crucial in attracting the public to contribute to the project. If it is hard to start, people might not be motivated enough to even finish a PR.
* Little details matter. It makes it easier for the project team members to review the PR if you provide sufficient details on the fix. For example, providing a screenshot for the new feature that you have added, allows the reviewers to have a basic idea of how your fix will improve the project. They are therefore more likely to review your PR (because it takes less work to get into the context) and see it into completion.
* Contribute with an open mind. Big projects can be difficult to navigate around even with documentations, so you are highly likely to get things wrong the first time regardless of how prepared you are.

## Workflow for Chrome migration in Electron

The electron project periodically upgrades the Chrome version to the latest version available. One such PR that does such an upgrade is as follows:

https://github.com/electron/electron/pull/8406 [involves moving the build system from gyp to gn]

While this PR might appear to be linear and done in one shot, in actual fact, it is a result of multiple smaller PRs combined together. Some of the commits in this PR comes from other smaller PRs:
* https://github.com/electron/electron/pull/8367 [adjustments made due to new build system used]
* https://github.com/electron/electron/pull/7909 [actually the inital PR, but it got absorbed into PR 8406. **NB:** Ideally, this PR should be the one absorbing PR 8406, since it is mainly responsible for upgrading the Chrome version]

This give rise to an informal workflow, whereby multiple developers can collaborate in parallel on the same area (moving to the new Chrome version) but dealing with different issues (importing the new files, changing the build system, etc). Developers work separately on their own smaller PRs. When it is completed, it does not get merged into master straight away. Instead, the PR is closed, and the commits made in the smaller PR is absorbed into the final big PR. Changes made in one PR can be carried across to another PR (through git branches). This allows us to "save" the progress of smaller PRs.

The workflow serves a critical purpose of ensuring that the fix are for a version of Chrome that is consistent with the current version used in the repository, and not being pushed to master ahead-of-time (which might not make sense or even work if the changes are new API calls/behaviors/etc...).

## Suggested Workflow to se-edu (Internal Project): Epic PRs

In se-edu, there is always a concern, when encouraging developers to split a potentially large PR to smaller PRs, that the developer may abruptly leave halfway, leaving the repository in an inconsistent state.

Therefore, the workflow described above can be useful when implementing a big feature. The smaller PRs do not need to be immediately merged to master once done, but should be absorbed to the final PR (let's call this the "epic PR"). That way, smaller PR can still go through our rigourous review process. They do not need to be reviewed again in the epic PR unless necessary.

By adopting this workflow, it is possible for future developers to pick up and continue the epic PR in case the original developer leaves the project team. The epic PR also allow us to avoid weird scenarios whereby the repository is migrated halfway, and is still using the old system because the new one is only half-done.
