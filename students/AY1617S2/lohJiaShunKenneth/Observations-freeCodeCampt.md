# Contributing to freeCodeCamp

## freeCodeCamp

[freeCodeCamp](https://www.freecodecamp.com/) is a website to teach people how to learn coding, through online lessons and resources. Users will learn how to develop software engineering skills in HTML5, CSS3, JavaScript, Node.js, React.js, D3.js, as well as learn use databases and Git, and from there move on to full-stack development. This is done through the many interactive courses, tutorials and resources provided on the freeCodeCamp website.

The resources the website provides are totally free, and as such it relies on donations, as well as crowd-sourcing to help develop its lessons.

## About the Codebase

freeCodeCamp is an online platform, and hence the codebase comprises of mostly HTML, CSS and JavaScript. Each chapter is implemented as a Json file which defines the contents of each lesson. These lessons run on a framework so as to maximize code re-usability, while making development easy through the modularity of lessons.

## Workflow Links
The contributing guide can be found [here](https://github.com/freeCodeCamp/freeCodeCamp/blob/staging/CONTRIBUTING.md).

## Workflow Summary

Contributing to the codebase can be summarized in the following steps:

Setting Up
1. Install MongoDB and Node.js, and make sure they are at least version 3 and 6 respectively.
1. Fork the freeCodeCamp project and clone that on your computer.
1. Read the contribution guidelines.

Contributing
1. Find an issue on freeCodeCamp’s Github page.
1. Post a comment on the issue to indicate that you are working on the issue.
1. Branch from the updated staging branch.
1. Implement/fix the relevant issue.
1. Run the tests.
1. Squash your commits.
1. Create a pull request (PR) with the following format:
	* Pre-Submission Checklist
		* Your pull request targets the staging branch of freeCodeCamp.
		* Branch starts with either fix/, feature/, or translate/ (e.g. fix/signin-issue)
 		* You have only one commit (if not, squash them into one commit).
 		* All new and existing tests pass the command npm test. Use git commit --amend to amend any fixes.
	* Type of Change
		* Small bug fix (non-breaking change which fixes an issue)
		* New feature (non-breaking change which adds new functionality)
		* Breaking change (fix or feature that would change existing functionality)
		* Add new translation (feature adding new translations)
	* Checklist:
		* Tested changes locally.
 		* Closes currently open issue (replace XXXX with an issue no): Closes #XXXX
	* Description

1. Two Issue Moderators from the core team will go through PRs for quality assurance.
1. Fix any issues with the PR if needed.

## Lessons from working on freeCodeCamp

### Communicating effectively

Working online without meeting face-to-face means that it is hard for people to ask questions when explaining things to people. Most, if not all, forms of communication exists through discussions on issues or PRs, where replies take hours or even days.

Learning to explain things in a comprehensive yet concise manner helped me to communicate my changes effectively. It is also good to pre-empt questions, and answer them in the explanation so as to prevent time wasted asking for clarification, and answering them.

### Self-learning

As discussed earlier, communication through Github is not efficient. As such, not all project requirements or expectations are communicated.

Firstly, I had to explore the codebase a little so as to understand the structure of the platform, as well as how to implement changes that work with the codebase. This is contrasted to working with PowerPointLabs, where we can conveniently ask our peers about how their portion of the code works.

Secondly, not all the coding styles are explicitly stated, and hence I had to infer the style expected of the changes I was making. This could be done by setting up Linting, reviewing existing code in the codebase, as well as reviewing the feedback made on similar changes on the project.

Lastly, I had to learn the working culture of the project, through observing the communication within the project. For instance, I learnt that making an issue then asking to work on it is not a hard requirement. In fact, sometimes people will "steal" the issues I was working on, by creating a PR before I made mine. However, people making PRs with style violations will be made to rectifying them before allowing the merge.

### Every little detail matters

Despite being a large-scale project, freeCodeCamp focuses not just on large features, but also the small changes. Small changes such as "tutorial title slightly ambiguous" are also raised as issues to be fixed, minor style violations are not tolerated, and fixes that work will still be questioned if it is the best way to do it. There is very tight quality-checking in this project even though it is a free service being developed by volunteering coders.

I think this may be because small discrepancies and errors build up over time to create technical debt and bugs that are hard to fix without huge amounts of refactoring. With that in mind, I needed to think about developing in a way that is consistent with the existing codebase, instead of simply making the issue go away. This is hard because some of the changes I had to make were different from existing code. Hence, I had to figure out how to code fixes that will work well with the modular structure of the codebase.

## How PowerPointLabs can be improved

After working in both PowerPointLabs and freeCodeCamp, I want to suggest some changes to improve the workflow of PowerPointLabs.

### Better communications
In PowerPointLabs, we work in a small team that meets weekly. As such, majority of the updates and changes we made are communicated well, and we can ask each other about the things we do. However, this means that newcomers to the project will be lost when they try to contribute to the project, especially if they are working remotely instead of joining the team physically.

By having more documentation of our progress, newcomers can also join in the contribution with less friction.

### Systems and checklists
The checklist system is very useful in both summarizing the changes made so that the reviewer spends less time on each issue, as well as reminding the person making the PR to do all the required testing and checking before making the PR.

### Stringent standards
We should be strict in our standards, both in developing and reviewing. This has not been the case in the past, and hence there is a lot of technical debt with poor code organization and naming.

### Repaying technical debt
Refactoring the various portions of the code in PowerPointLabs should be a priority. The coding styles should be standardized, and the old labs should have files named according to our standaridzed naming convention, as well as placed in their respective folders.

## Conclusion

Working on these two OSS projects have exposed me to more forms of working environments. It is a change of pace as the workflow of these projects are very different from that of the corporate environment which I am used to. Perhaps in future I may contribute to more OSS projects as it is a good way to contribute to something useful, as well as improve my coding skills.

