# Observations on pdf.js workflow

The contribution guidelines for pdf.js can be viewed [here](https://github.com/mozilla/pdf.js/wiki/Contributing). This document will solely focus on the advantages/disadvantages of the contribution workflow of pdf.js.

The observations can be split into two components: Issue and Pull Request workflows.

## Issue workflow

### Issue template

One notable difference to PowerPointLabs is that pdf.js makes use of an issue template [(click to view)](https://github.com/mozilla/pdf.js/blob/master/.github/ISSUE_TEMPLATE.md), which turns the issue tracker into a more standardised issue reporting system. On top of that, this allows external users (for instance, developers embedding pdf.js) to report bugs and suggest new features in the same issue tracker. As such, this allows developers/contributors to focus only on a single place, which would be the issue tracker, rather than having to monitor multiple channels.

This component of the workflow would prove useful for PowerPointLabs, as the current workflow for PowerPointLabs uses two different avenues for reporting issues to the developer -- email and the GitHub issue tracker. As only the core team has access to the mailing list, other contributors may not be informed of the bug that needs to be fixed, unless a core team member posts the issue on the tracker. On top of that, using a template allows for standardisation of information that is collected in each issue (for instance, screenshots of the bug, stack trace or steps to replicate problem), which ensures that enough information is collected such that the developers/contributors can start solving the issue.

### Labels

The pdf.js issue tracker makes use of a minimal set of labels to categorise/tag issues. The labels are used to tag issues based on things like: the type of issue (if it's not a bug), bug type (e.g. broken pdf), platform (e.g. firefox, ie specific) and so on. As such, the labels convey useful information about what the issue is about and does not cause a clutter on the issue tracker.

Currently, PowerPointLabs has labels for priority of issues. However, in the interest of ensuring that the labels convey meaning, these labels should be removed, as there's no value add to the issue being labelled. The fact that the issue is in the issue tracker means that it is a feature that is worth fixing and it would be good if an easy bug (that is marked as low priority) is fixed if it is trivial, rather than to prioritise bugs that may have a complicated fix/solution. As such, this would allow the project developers to clear out the backlog of issues as efficiently as possible.

On top of that, other labels, like platform and effects of bug (e.g. program crashes or corrupted file), could be added into the current set of labels. This would allow developers to pinpoint the root of the problem efficiently and to not cause the bug to remain unfixed due to a lack of focus as to what is the bug and which version does it affect.

## Pull Request workflow

### Bots

pdf.js makes use of [bot.io](https://github.com/arturadib/botio) to run certain tests, on top of utilising Continuous Integration. The purpose of using this bot is to allow the use of an external, self-provisioned test server. Furthermore, the bot is manually triggered and as such, would only run if requested.

This bot (or at least, this type of bot) may be useful in both TEAMMATES and PowerPointLabs and the reason for recommending this solution is different for the two projects. For TEAMMATES, using a bot would ensure that certain tests (for instance, UI), that are time consuming, would only be run after the pull request has been approved. This reduces the number of test runs, most of which would not matter, as the pull request may not be approved yet. However, in the case of PowerPointLabs, utilising such a bot could help in automating certain tests that requires PowerPoint to be installed (for instance, feature tests). As such, there would be less of a need to rely on approval from certain developers that are developing for certain versions of PowerPoint.

### Testing

An unwritten rule of pdf.js is that every bug fix requires a test case (or suite), so as to protect bug fixes from further regressions. 
