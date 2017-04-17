# Contributing to Webogram (Telegram Web)

Author: [John Yong](https://github.com/whipermr5)

Contributions:

*   [`Double click to scroll to bottom of conversation. Fix #1335`](https://github.com/zhukov/webogram/pull/1360)
*   [`Update message preview on message edited. Fix #1177`](https://github.com/zhukov/webogram/pull/1378)
*   [`Implement unsend messages. Fix #1340`](https://github.com/zhukov/webogram/pull/1379)

## Contribution Guidelines

I use [Telegram Web](https://web.telegram.org) on a daily basis and was pleasantly surprised that it is an open source project, named [Webogram](https://github.com/zhukov/webogram). Their contribution guidelines can be found [here](https://github.com/zhukov/webogram/blob/master/CONTRIBUTING.md).

## Learning Points

### Contributor Squashes Commits

Contributors are encouraged to make as few commits as possible, and squash and rebase whenever requested changes are made. While this makes the commit history clean, making it easier to review, it loses history of the different approaches the contributor might have made and how he decided on the current approach.

This made me grateful for TEAMMATES' flexibility in allowing lots of commits in the PR, only squashing and merging at the final step when the PR is merged. The decision-making history is also preserved by GitHub through the conversation thread.

### Looser Adherence to Workflow

Even though the guidelines are clearly spelt out in the document (e.g. including the issue number in the PR), these are not always followed. Merging is carried out according to the discretion of the maintainer. There are also no guidelines in place regarding when a PR will be reviewed or merged.

While this means less commitment on the part of maintainers and more freedom to focus on what they deem to be important for the project, it also gives contributors a sense of uncertainty regarding when their PRs will be reviewed or merged, if ever.

### Lack of Developer Documentation and Testing

The maintainer seems to favour PRs that implement new features a lot more than other kinds of PRs like fixes and tests. The first few PRs I submitted were fixes, which were reviewed very slowly. It was only after I submitted the feature PR that the maintainer started taking notice of my other PRs.

One PR submitted by another contributor did not implement any new features, but laid the groundwork for future features to be implemented (it was an update to the Telegram API schema which was required for several new features). This was closed on the basis that it did not implement anything new. It should be bundled with the feature that actually requires it. My feature required it, but I was unaware that it had already been implemented but not merged until the author commented on my PR. I subsequently bundled it together with my PR and it worked flawlessly. But time had been wasted wondering about how to go about doing the schema update.

As can be seen, the focus on features actually backfires in the long term, as the general lack of groundwork makes it very hard for new developers to get started. New features are very slow in being implemented (my feature PR implements the unsending of messages which has been around in the other native mobile/desktop Telegram clients since January; the issue to support skin-toned emoji is already 2 years old but still there has been no good attempt at it).

This is due to a lack of developer documentation - I had to pore through the code for an entire day just to get a brief idea of the various components and implement a tiny fix. The codebase is quite huge but has very few comments. Tests, which usually help to document the code, are also missing. These things made me grateful for TEAMMATES' good documentation and substantial test suites. While I dislike writing comments and tests, this experience showed me how important they are. If I didn't take the effort to do them right, my future projects would also look like this.

Having said that, the maintainer has acknowledged the need to add tests, and accepted a couple of PRs that implement them. The discussion can be seen [here](https://github.com/zhukov/webogram/pull/1293).

## Practices that can be adopted by TEAMMATES

### Clean Commit Messages

As mentioned earlier, the commit history of Webogram PRs is very clean. While I do not agree with the extreme of one commit per PR guideline, I feel that TEAMMATES can still be slightly stricter with regards to commit messages. The fact that all PRs are squashed and merged with commit message set to the issue title may have bred laxity in our commit messages within PRs. A solution might be to enforce cleaner commit history for more senior developers.

### Curated Issue Tracker

The maintainer is very proactive in cleaning up the issue tracker, for example, closing duplicate issues and providing reasons why issues are not accepted. It reminded me of TEAMMATES' issue tracker, which has hundreds of issues over two years old. There is probably a need to go over some of them to verify if they are still valid.
