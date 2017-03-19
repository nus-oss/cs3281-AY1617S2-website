# Contributing to Open Source: freeCodeCamp
---

## Introduction

freeCodeCamp is a friendly open source community where users learn to code. It features a website where users can work through self-paced coding challenges, build projects, and earn certificates. Their goal is to aid the public in building job-worthy portfolios of real apps used by real people, while helping nonprofits. Established in 2015, it has grown to have over 800,000 registered users, with almost 400,000 being active. You can read up more on freeCodeCamp [here](https://www.freecodecamp.com/about/).

Note: While I was contributing to this repository, freeCodeCamp was in the process of moving to its [beta site](https://beta.freecodecamp.com/en/map). All PRs made to the repo currently aren't live on the main site, but will be once beta is released.

## Contributing to freeCodeCamp

The site itself is written in mostly Javascript, CSS and HTML, so some knowledge in web development is needed to contribute to this repository. freeCodeCamp is geared towards teaching users many front-end frameworks, so ideally some experience with them would be useful. Most of the content is contained within the code challenges, which are represented by JSON objects. This makes the codebase very modular and easy to make changes without having to understand the entire system. Minimally, familiarity with JSON is required, as all challenges are formatted that way. The link to to the repository can be found [here](https://github.com/freeCodeCamp/freeCodeCamp).

freeCodeCamp treats their Github repository as a second avenue for their users to pick up software development skills, and they even have a course for using Github. Users are thus encouraged to make their own contributions to the site, and the moderators are very helpful and beginner friendly, as they want to encourage first timers to contribute to open source. The procedure for setting up the working environment and making a PR is clearly documented [here](https://github.com/freeCodeCamp/freeCodeCamp/blob/staging/CONTRIBUTING.md), along with places to seek help if one gets into trouble.

### Summary of contributing workflow

Here is a short summary of the contributing workflow:

1. Find something to work on:
    * Suggest a feature or bug you'd like to fix. You will be given a short checklist to fill out with information such as description, browser info, screenshots, etc.
    * Find an existing issue to work on. Recommended tags are `help-wanted` and `first-timers-only`. Leave a comment saying you'd like to work to it.
1. Wait for the go-ahead from one of the core members.
1. Create a fork of the `staging` branch and make changes.
1. Test changes locally and ensure all tests pass.
1. Create a PR against the `staging` branch. You will be asked to fill in a checklist. Three important things to ensure:
    * Your branch name must start with `fix/`, `feature/` or `translate/`
    * You have only one commit (squashed)
    * Branch targets the `staging` branch
1. The PR will be labelled as `QA`. Wait for a member to review.
1. Upon review:
    * If the PR is accepted, it will be automatically merged and closed.
    * If the PR is rejected, you are given a list of changes to make. Make the changes, and use `git commit --amend` and `git push --force` to push them (Don't make a new commit)

## What I've learnt

### Not every contribution has to be a large one.

I was actually quite surprised at how receptive the admin team was in responding to suggestions, even for minor ones like minor wording errors. For any large project or repository, many things can be improved, and even the small things can make the project a little better. I find that a common belief amongst many coders nowadays is that it's not worth wasting time on things that aren't broken, and that it's better to focus on the bigger things like new features and breaking bug fixes. While true, it doesn't make little fixes any less beneficial, as these add polish and quality to the code base in general. These really help in improving the user experience, both for users and developers alike.

### Don't be afraid to share your suggestions.

One main deterrent that stops many programmers from contributing to open source is that they're afraid of sharing their code. Creating an issue and a PR usually leaves you open to other coders to comment and judge your work, and that's never a nice feeling. While there are a few unsavory people who might be overly judgemental, there are also many who are willing to guide you and offer a helping hand. The point of open source is to encourage coders to share their code (and for free), so people aren't as critical of mistakes as you would think. Even though a few of my PRs had a lot of things that need fixing, I felt that most of their criticisms were fair, and they pointed them out respectfully and without ill intent. I can safely say that contributing to freeCodeCamp has helped me improve my coding skills.

### Learn to learn.

It's hard to get into a new project. The first step, setting up the project and understanding the codebase is usually the hardest, and the problems you encounter are usually unique to your system and not documented. It's frustrating, but I think working with external open source projects offers an experience that a comfortable school project environment would never provide. You learn how to troubleshoot, look for help, and solve problems on your own. These are all vital skills in learning new how to operate new frameworks and projects, and are very applicable to programmers since new technologies pop up all the time. I usually say that a good programmer isn't one who's proficient at what he's used to, but rather one who can be given something he has never used before and instantly learn it. Open source offers good training in this aspect since pretty much every single repository uses a different stack and workflow that needs learning.

Other small notes/interesting details:
    * If you need a response/review from someone, tag him/her. Don't be shy and just silently commit changes. Otherwise your PR won't be reviewed for weeks.
    * Conventions may be there, but they aren't always followed. In the few weeks I was surveying the issue and PR lists, I've observed many people who neglected to read the docs and just did whatever they liked. Surprisingly, the admins didn't really have much problem with this, as long as it didn't cause trouble. I guess results trumps bureaucracy at the end of the day.
    * When it doubt, make a PR anyway. The admins may not have time to look through issues, but they'll definitely review PRs.
    * freeCodeCamp is a place for coders to learn GitHub, so many new issues get snapped up really quickly. The admins don't mind who does the work as long as it gets done, so they go by first come first serve. One practice I had to adopt was to make an issue, then make a PR as soon as possible. I wouldn't recommend doing this on other repositories, but when grades are involved you have to be a little competitive =).
    
## Comparison to NUS-OSS

What's interesting about freeCodeCamp and NUS-OSS is that they share similar goals. Both are repositories intended to introduce fresh coders to contributing to open source. As such, many of their practices can be applicable to NUS-OSS. For this section, I will be talking about freeCodeCamp in contrast with PowerPointLabs, which is the OSS project I'm working on.

* **Well documented setup** - freeCodeCamp has an entire page dedicated to helping developers setup the work environment, describing how to make a change/how a PR gets reviewed and resources regarding project conventions. Our project only has a short section on the instructions for setting it up. This might chase newer developers away from wanting to work on it, as they wouldn't know where to start.
* **Avenues for contributors to seek help** - freeCodeCamp offers [chat support](https://gitter.im/FreeCodeCamp/Contributors) for contributors to seek help when they get stuck. This can be helpful for developers who want to ask questions about the project. For PowerPointLabs, we use slack, but only privately amongst our own team. It would be nice to have public chat support for people to ask questions.
* **Squashing commits** - freeCodeCamp requires all pull requests to be squashed to one commit, while PowerPointLabs allows multiple commits in a PR. With squashing commits, this keeps the git history of the main branch (`staging`) clean when the pull request is merged, rather than having a chain of commits from every merged branch. However, it does make some of the larger PRs harder to vet through in future, and it also makes the contributing workflow more tedious. I'm unsure which is better, but this can be something we should consider.
* **Templates for issue and pull request submission** - When submitting a new issue or pull request, the default text contains a template. This helps guide the user in making a clearer and more thorough issue/PR, while ensuring the maintainers have enough information to make a judgement.

## Conclusion

freeCodeCamp is a great place for beginners to open source to start contributing. It offers friendly moderators, many avenues to seek help, and a well documented contribution work flow to get started. The code base is also very easy to get into, and doesn't require a lot of knowledge of javascript or HTML to contribute to. I have learnt a lot from contributing to freeCodeCamp, and I would strongly recommend freeCodeCamp as a repository for beginners to open source to start with.

## Links

Link to Github: [freeCodeCamp on Github](https://github.com/freeCodeCamp/freeCodeCamp)
Link to site: https://www.freecodecamp.com/
Link to beta site: https://beta.freecodecamp.com/en/
Link to contribution workflow: [CONTRIBUTING.md](https://github.com/freeCodeCamp/freeCodeCamp/blob/staging/CONTRIBUTING.md)
Link to my contributions: [Pull requests](https://github.com/freeCodeCamp/freeCodeCamp/pulls?utf8=%E2%9C%93&q=is%3Apr%20author%3Ajamos-tay%20)
