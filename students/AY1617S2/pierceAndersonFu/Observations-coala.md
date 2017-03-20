# Contributing to coala

## coala Workflow Documentation

- [Newcomers' Guide](http://api.coala.io/en/latest/Developers/Newcomers_Guide.html)
- [Development Setup](https://api.coala.io/en/latest/Developers/Development_Setup.html)
- [Enhancement Proposals](https://github.com/coala/cEPs)

- Formats and Conventions
    - [Codestyle](http://api.coala.io/en/latest/Developers/Codestyle.html)
    - [Review Process](http://api.coala.io/en/latest/Developers/Review.html)
    - [Writing Good Commit Messages](http://api.coala.io/en/latest/Developers/Writing_Good_Commits.html)
- 'How to' Guides
	- [Writing Documentation](http://api.coala.io/en/latest/Developers/Writing_Documentation.html)
	- [Writing Tests](http://api.coala.io/en/latest/Developers/Writing_Tests.html)
	- [Executing Tests](http://api.coala.io/en/latest/Developers/Executing_Tests.html)
	- [Adding CI to Your Fork](http://api.coala.io/en/latest/Developers/Adding_CI.html)

## Learning Points

The first thing that hit me was how much friendlier coala was when it came to onboarding new contributors. Newcomer guides are placed in prominent locations and easily accessible. Their guides are broken down into easy to follow steps, and tend to be self-contained so readers don't have to lost in a sea of links. New contributors are directed to the latest cEP (coala Enhancement Proposal) so they're aware of the project's current objectives. They have a public chatroom that anyone can join. 

I believe that se-edu can benefit from having a healthier more vibrant contributor community if we improved the way we interact with new contributors. Having first-timer issues is a good step in the right direction, but there's still more that we can improve on.

## Good Practices
Practices/tools of the external project that I think can be adopted by se-edu.

- *Newcomers' Guide*
	-  **Problem**: While se-edu relies on the guides and conventions for contributing on oss-generic, it is neither readily accessible from se-edu's Github pages nor is it specific to a given project. That means developers who wish to contribute to se-edu as an OSS don't have clear guidelines on how to contribute, even though they may have easy access to the code and extensive architectural diagrams.
	-  **Solution**: se-edu could stand to learn from coala in this aspect. Their newcomers' guide neatly breaks down the contribution workflow into steps, helping orientate new developers to their expected behaviours. se-edu should have such a guide that points users to our commit message conventions, and instruct contributors to use CanIHasReview when making PRs.
	-  **Benefit**: se-edu may in turn see more contributions, and see less rookie mistakes that require a more senior member to point them the right way.

- *cEPs (coala Enhancement Proposals)*
	- **Problem**: Whenever major features or changes are proposed for se-edu, they tend to discussed in person, written on whiteboards, or mentioned in PRs. This makes it hard for developers to follow any major revamps being planned, and these updates may catch them off guard. 
	- **Solution**: In coala, cEPs are used to propose and discuss new major features. After specifying features with a cEP they should be implemented as specified. Unspecified features should not be implemented. As part of the onboarding process of new contributors, they are also expected to have read the latest cEP. However, it is not evident how contributors can discuss about points in a cEP. With se-edu's implementation, it would be beneficial to have some way of fostering and storing discussions on enhancement proposals. A separate issue for each enhancement proposal could be used as a discussion thread.
	- **Benefit**: This would help new and senior contributors of se-edu understand in concrete terms where we are at as a whole, and what we're working towards at any given point of time. It serves as a reminder and guide to keep the project moving forward cohesively.

- *Public chatroom (Gitter)*
	- **Problem**: Newcomers to se-edu have no obvious avenues of support.
	- **Solution**: coala has a public chatroom with friendly members who are expected to follow the code of conduct. se-edu could benefit from allowing newcomers to discuss amongst themselves and senior contributors in a public chatoom.
	- **Benefit**: Newcomers can avoid feeling overwhelmed, and clarify first instead of making corrections later. Senior contributors can also get a feel of what newcomers are interested in, and common problems faced, which can then be updated in the relevant documentations.


## Suggested Areas of Improvement
- While similar to how se-edu has guidelines for the seemingly minutiae (e.g. formats for commit messages), coala could benefit from having more fine-grained guidelines. Topics such as code documentation style could benefit from being more explicit with their requirements. coala could also benefit from having an issue template, such that issues will contain more relevant information in an easily parsed format.
- coala does not appear to have a maintainer's guide, making it harder for contributors to transition over to become maintainers.
- After being reliant on CanIHasReview, it is evident that reviewing PRs in Github is a flawed process. It is difficult to review past iterations of a PR to understand how it has evolved and to compare differences between the current iteration and the previous. As such, new contributors lose out on the chance to learn from other people's mistakes in their PRs, and the reviewing process becomes daunting. Additionally, referring to commits via SHA can be hard to follow in a long thread.
- coala doesn't fully utilize Github's PR review features. It would improve their review process.
- coala doesn't have architectural diagrams, making it harder for developers to see the bigger picture.