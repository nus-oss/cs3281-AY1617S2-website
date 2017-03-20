# What I've learnt from contributing to scikit-learn

## Scikit-learn Workflow Documents 

[Scikit-learn](http://scikit-learn.org/stable/index.html) has an excellent [developers guide](http://scikit-learn.org/stable/developers/index.html). This [chapter](http://scikit-learn.org/stable/developers/contributing.html) describes the workflow process.

## Learning points

* Scikit-learn has high standards for its documentation. Since it is a library primarily for non-data scientists to use machine learning, the documentation must both explain what each algorithm does, while also providing the mathematical details for experts.
* It is possible to get started even with limited knowledge in the subject.
* Good documentation is very important to orient new contributors, especially for large OSS projects.
* API design is very important - Scikit-learn's uniform estimator API makes it much easier to use and learn. This would be harder for applications like TEAMMATES though.

## Things from Scikit-learn that can be adopted by TEAMMATES

* Improving documentation would make it easier for new developers to learn the codebase. In particular, some things Scikit-learn has done that would be useful are:
    * Browsable HTML documentation generated from the code
    * A [utilities for developers](http://scikit-learn.org/stable/developers/utilities.html) page lists frequently used functions. For example, input validation, benchmarking and testing functions. Right now, finding this out would require working with the code base for a while to gain familiarity.
    * Documenting other aspects such as how to conduct performance profiling and making releases
* Scikit-learn has a deprecation process to move users to newer APIs. For example, I noticed that after working on [this PR](https://github.com/TEAMMATES/teammates/pull/6538), the old methods were still used in favour of the new methods introduced. A "Utilities for developers" page would also help here as well.
* Using PR titles for WIP / ready for review: since labels can only be used by commiters with write access, using titles instead would make it easier to find PRs that need to be reviewed.

## Suggested improvements for Scikit-learn

* Though the linters Scikit-learn uses are documented (e.g flake8, nose, pep8), it would be convenient if they could be automatically installed (e.g by using a requirements.txt file for pip), and ran all at once with a single command, like in TEAMMATES. This makes it easier to push passing code.
* Enforcing a format for issue titles makes it easier to associate PRs with issues. A bot could also be set up for this.