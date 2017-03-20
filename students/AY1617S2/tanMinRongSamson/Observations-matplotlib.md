# Observations on matplotlib's workflow

> matplotlib's workflow document can be accessed [here](http://matplotlib.org/devel/index.html).

In this article, I discuss the workflow of `matplotlib` and some practices that may be beneficial by TEAMMATES.

### Learning Points

After contributing to `matplotlib`, I realized the importance of having a community of developers available to look at our code. As a new contributor who is less familiar with the codebase, there are often better ways of fixing an issue than what we initially come up with. Having other developers review our fixes not only helps us catch potential bugs in the fix, but also helps with producing a better (more efficient/readable) approach to the problem.

### Observations that may be beneficial for TEAMMATES

##### Use of `WIP` and `MRG` tags

matplotlib makes use of `WIP` and `MRG` tags in the PR title to signal the PR's status to the maintainers. This allows the maintainers to see, at glance, which PRs are ready to be reviewed. This is a huge time saver for repositories with high traffic and maintainers that are mainly working adults. Although TEAMMATES has a label system, this requires someone with write access to keep track of the PRs and update the labels. A possible way to shift the work of tracking a PR's status to individual contributors is to get contributors to include a `WIP` / `RVW` tag within their PR description. `teammates-bot` will then detect these tags and update the labels automatically.
 
 
##### Preserving PR's commit history instead of `Squash and Merge`

TEAMMATES can benefit from preserving the commit history of large PRs instead of simply squashing them into a single commit. Future bugs can be tracked down and fixed more easily if the commit history is not squashed. However, this will demand an increased standard for commit messages written by contributors, or else it will result in an extremely messy commit history.

#### Improvements to matplotlib's workflow'

##### Standardized commit message format
 
 Currently, contributors seem to be allowed to write whatever they want, and many different formats are used. E.g. first words are capitalized in some commits but not others. This makes the history messy and difficult to follow at times. `matplotlib` should establish a standard commit message format that all contributors must follow, e.g. oss-generic's conventions. This, combined with preserving the PRs' commit histories, will help greatly in tracking down bugs.

##### Adopt the one logical change per commit guide

This relates to the overall theme about preserving commit histories. Since PR commit histories are preserved, implementing the one logical change per commit will further improve bug traceability and improve review turnaround times.
