## Observations: CheckStyle Project

CheckStyle is a static analysis tool that is used in many projects, or even in industry. It is a project since 2007 and till now its code quality has reached a fairly high level. The project is maintained by a professional team and they welcome contributions.

### Overall contribution workflow

#### [Set up]( http://checkstyle.sourceforge.net/beginning_development.html)

CheckStyle assumes developers to familiar with Java, JUnit and Maven. Therefore, the setting up guide tends to be simple. There are [overall development guide](http://checkstyle.sourceforge.net/contributing.html) and separated setting up guide for different IDEs including [Eclipse](http://checkstyle.sourceforge.net/eclipse.html), [NetBeans](http://checkstyle.sourceforge.net/netbeans.html) and [IntelliJ](http://checkstyle.sourceforge.net/idea.html). They all describe things in high-level. The details, such as how to install plugins and how to use different commands in `maven` are left to developers.

#### [Report an issue](http://checkstyle.sourceforge.net/contributing.html#Report_an_issue)

CheckStyle accepts bug reports but doesn’t accept feature request currently. As described [here]( https://groups.google.com/forum/#!topic/checkstyle-devel/JbhfiiSqKsQ), a new feature requires a lot of testing and revising. Only the mirror project ([Sevntu.Checkstyle](https://github.com/sevntu-checkstyle/sevntu.checkstyle)) accepts new features (checks).

#### [Submit contribution]( http://checkstyle.sourceforge.net/contributing.html#Submitting_your_contribution)

It’s not all issues that can be worked on. Contributors can only submit fixes for issues that are marked with `approved` tag. Developers are required to follow a certain format in PR title and commit messages. To ensure quality, the project requires developers to run `mvn verify` before submitting PR. Additional checks such as test cases in different locals, test cases in different operating systems and static analysis in IDEA will also be evaluated for the PR to pass.

### Learning Points

#### Good guide will attract more developers

CheckStyle project is not a good example in this case. It doesn’t have a good developer guide. Information such as how checks work, how to set up IDE, how to submit PR is all over the places on the website. Developers would need to search this information by themselves, which would scare new developers away. From my observation, besides core team, there are only several commits per month from outside people. Though I admit that experienced developers could quickly find the information and this mechanism may filter out inexperienced people in some measure, it is never a bad thing for an OSS project to have a friendly guide.

#### Write good commit messages

Writing good commit messages is important in CheckStyle. I once submitted a [PR](https://github.com/checkstyle/checkstyle/pull/3957) containing a fix and several test cases. I separated my fix and test cases in several commit messages. I was required to squash them into two commit messages (fix and test cases) to ease the review. Indeed, commit messages are not only for developers to keep track of where are they, but also provide a good way for reviewers to review.

#### Quality Matters

In my [PR](https://github.com/checkstyle/checkstyle/pull/3957), we had a long discussion about how to test enumeration. My initial attempt was to write test cases to verify the number of enumerations in `Enum` and then test each enumeration individually. The project manager thought this approach was not effective enough as when new enumeration was added, developers might only change the number but fail to update the individual test case for each enumeration. They would still pass the test but bug might be introduced. He asked me to use `switch` statement and fail the JUnit test in `default` branch. Obviously, this approach is more effective though my initial attempt works.

#### Too many checks for PR is not always a good thing

CheckStyle has 7 checks for PR processing including 3 CI checks, 2 coverage checks and 2 static analyser checks. On the one hand, this makes reviewer’s works easier as it makes sure the App works in all environments. On the other hand, it seriously delays the progress of the project as it takes almost 1 hour for all checks to run. In addition, the checks will fail randomly sometimes due to timing. For contributors, the only way to fix this is to rebase and rerun all the checks. Furthermore, some checks like IDEA and wercker are not accessible to developers locally. The only way to see the errors is after all builds have finished.

### Adoptable practices/tools

#### RSS system, User Group Forum and Social Media Account

CheckStyle has User Group Forum, RSS system and official social media account, which are ways to connect developers and to update end-users. TEAMMATES now actually uses the issues tracker as a forum. Recently, it may also be a way to notify GSoC candidates. This may work fine for a small number of contributors. However, since the number of contributors grows, it could be messy to mix all the things together. It would be good if we have a separated discussion forum for developing help and have some social media accounts to update the users.

#### Format of commit messages

CheckStyle has several rules for commit messages and there is a Junit test for commit validation. Good commit messages may ease the review. It would be good to write a bot or test to validate commit messages in TEAMMATES.

#### Automation in release

When build is successful in `master` branch, CheckStyle will automatically do release update for maven repo. This automation can be used in TEAMMATES also. We can automate the deployment and testing in `release` branch.

### Suggestions to CheckStyle project

#### Reorganize the developer guide

It may be good to reorganize contribution guide to a friendlier version to attract more contributors. In addition, the community can also compile a trouble shooting guideline for new developers. Have something to refer is always better than figuring it out by themselves. Furthermore, there also could be some documentations showing the design of the application in a high-level way. 

#### Format of commit messages

Although it is good to require commit message to start with issue number as we can know who is working on the issue, frequently rebase would mess up the issue page with many useless commit messages. Instead of referring issue in a commit message, developers can be required to comment on the issue to show they are working on it. In addition, contributors can also refer to the issue in the PR itself to link the issue and PR together.

