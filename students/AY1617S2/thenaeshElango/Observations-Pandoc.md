# Observations of Pandoc's Workflow

## Guides

Pandoc has a [contributor guide](https://github.com/jgm/pandoc/blob/master/CONTRIBUTING.md)
that is required reading for all new contributors.

The document mentions the expected workflow for submitting a patch to Pandoc. Key points are:

* A patch is expected to consist of a single, well-explained commit, though this rule is sometimes
ignored.
* The style guide is rather interesting: it simply asks contributors to follow the style guide
already present in the surrounding code, rather than explicitly documenting style guide in a specific
place.
* Any new feature, no matter how small or trivial, is expected to come with an update to the user manual.

A reasonably comprehensive overview of the codebase is given at the end of the contributor guide.
It gives details of what each file contains. One advantage of Pandoc being written in Haskell and
having a linear code path is that this is generally sufficient documentation, and any further details
can be easily found by reading the type definitions in the code itself.

## Issue Management

There are the usual tags on issues such as `beginner-friendly`, `enhancement`, `bug`, `complexity:low`,
`complexity:high`, etc.

One interesting point is that there is the `status:more-info-needed` for
incomplete bug reports and `status:more-discussion-needed` for issues for which that way to solve
the problem is not clear. The result is that quite a lot of discussion happens on the issue tracker,
in public for all to see.

## Project Organisation

There is one benevolent dictator, who is extremely friendly and welcoming to new contributors.
There seem to be several others wih commit access to the main repository, but commits from them
are extremely rare.

## Tools

Standard tools such as Travis and AppVeyor are used for build management. Travis failures are taken
far less seriously than in TEAMMATES, though, as there is often some misconfiguration in Travis.

## Areas of Improvement for TEAMMATES

TEAMMATES has the habit of having major project discussions in private IRC channels. This makes it
harder for new, external contributors to keep track of major changes that are about to happen (especially
when there is virtually no discussion on the issue/PR itself, and the title looks fairly innocuous).

If it is possible to still move fast while having discussions entirely in public (there is no reason why
this shouldn't be possible), then it may be a good idea to do so, for the benefit of external contributors
interested in the area being discussed.

Simple issues and fixes can skip the standard 3-level review process, as this is largely a waste of time.
The standard process should remain for non-trivial issues, though. Pandoc has an informal review process,
where patches are reviewed quickly if they are small. If they are larger, there may be more committers
helping to review them.

## Areas of Improvement for Pandoc

Travis should probably be set up properly, so that tests can be a proper arbiter of the quality of a PR.
