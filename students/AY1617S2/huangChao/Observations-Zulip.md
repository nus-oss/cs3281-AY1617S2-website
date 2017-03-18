# Observations - Zulip

Author: [Huang Chao](http://github.com/chao1995)

## Get Started

* Know what is Zulip project by briefly reading through [README on GitHub](https://github.com/zulip/zulip).
* Play with the [Live Demo](https://chat.zulip.org), which also serves as the primary communication forum for the Zulip community.
* Zulip maintains an exhaustive [Docs](https://zulip.readthedocs.io/en/latest/index.html). The must-read ones are:
    <ul style="margin-bottom: 0px">
      <li><a href="https://zulip.readthedocs.io/en/latest/dev-overview.html">Setup Local Development Environment</a></li>
      <li><a href="https://zulip.readthedocs.io/en/latest/architecture-overview.html">Architectural overview</a>. Watch out for concepts (e.g. streams, realms), tools and technologies in use.</li>
      <li><a href="https://zulip.readthedocs.io/en/latest/version-control.html#commit-discipline">Commit Discipline</a>. How to organize your commits so it's easier to review. How to write your commit messages.</li>
      <li><a href="https://zulip.readthedocs.io/en/latest/code-style.html">Code style and conventions</a>.</li>
      <li><a href="https://zulip.readthedocs.io/en/latest/testing.html">Testing and writing tests</a>.</li>
    </ul>
* First-PR workflow:
    * Sign the [Dropbox Contributor License Agreement](https://opensource.dropbox.com/cla/).
    * [Finds an issue you GitHub, labeled with `bite-size`](https://github.com/zulip/zulip/issues?q=label%3A%22bite+size%22). If nobody is working on the issue && the issue interests you, leave a comment saying you are willing to work on it.
    * Create a new branch, add your commits, and submit a Pull Request.
    * Wait for other developers' code review and make requested changes.

## Important things I learned from contributing to zulip

* You don't have to (or you won't have time to?) know everything before you start contributing to a large codebase. Just know enough to get the work done. You can always study the rest when you have extra time.
* Follow up quickly with the code reviewers.
* Testings are important. I write much more lines of testing code than the production code.
* "Monkey see, monkey do". More formally, follow the convention. You can see how other tests are written to write your tests.

## Practices/tools of Zulip that can be adopted by NUS-OSS projects

* No coupling with specific IDEs/Editors. Both TEAMMATES and SEEDU are using Eclipse as primary IDE, but some developers prefer to work with an editor because it's usually faster.
* Use Vagrant/Docker. This can potentially avoid lots of questions on GitHub issues for difficulties in setting up TEAMMATES, due to different environment settings.
* Comprehensive documentation using readthedocs.io, with handy features like search and version management of documentation.
