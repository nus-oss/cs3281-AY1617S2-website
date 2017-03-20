# Observations about workflow of SymPy

## Workflow documentation

SymPy's documentation on development workflow can be found [here](https://github.com/sympy/sympy/wiki/Development-workflow).

## Learning Points

* Having a high level developer guide is important, especially in a project with a large code base. Although functions and modules are well-documented with detailed docstrings and tests, there is limited high-level documentation. This makes it difficult for a beginner to have a grasp of how the different parts work together, and to understand the flow of the code, since even simple features (e.g. factorising an expression) can involve code from many different files.
* Contributing to an OSS project includes more than just contributing code or filing bug reports. They include things like writing documentation, answering other people's queries, reviewing pull requests and maintaining websites.

## Practices/tools that can be adopted by your NUS-OSS project

* When opening a pull request, a template is provided for the PR description. The template reminds developers to include the issue number and provide descriptive titles. We can consider creating a template for commit messages, since we have more complicated commit message requirements.

## Suggested improvements for SymPy

* Make documentation for development workflow more layered to cater for developers with different amounts of experience. Currently, important information for all developers, such as the naming format for branches, is interspersed with information that is useful for beginners, such as how to create a branch. While this makes it very helpful for beinners, it makes the documentation unnecessarily detailed for non-beginners since it is difficult to skim. This makes it less convenient for developers to find specific information.
* Increase standardization e.g. pull request titles, commit message formats. Different commit messages use different tenses and formats,
which makes the commit message history look untidy and harder to read.

