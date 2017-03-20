# Reflections after working on WordPress-iOS


## Links to any online documents about the workflow of external project:
Mainly: https://make.wordpress.org/mobile/handbook/pathways/ios/how-to-contribute/
For curiousity's sake: https://make.wordpress.org/mobile/handbook/general-guides/release-cycles/

The workflow is extremely similar to that of teammates, but they have an extra develop branch which is merged to master only after release. 

## Important things you learned from contributing to that project, if any:
Setting up is never easy. Similar to teammates, I had to create a test application, but I also had to obtain a client Id and client secret key for authentication purposes. Doing this with no prior experience to Wordpress was quite challenging and I was lucky to find a very helpful [guide](http://pinkstone.co.uk/how-to-build-wordpress-for-ios-2015/).

Even after the dependencies have been installed, the build still fails in the future when dependencies get updated. There was once where I had trouble getting cocoapods to work for the dependencies despite an initial successful setup, because certain ruby gem was failing. I had to learn and troubleshoot ruby issues even though I was working in Swift/Obj-C. I learnt to be resourceful, looking up error messages on google, trawling througn stackoverflow answers to see what could help. Eventually, I managed to solve a small setup problem and got the build to work, which was extremely gratifying.

Working on a new OSS project made me realise how useful tags are for understanding the scope of the issue. Similar to teammates, they use continuous integration tests for submitted PRs, just that they use buddybuild instead of travis.


## Practices/tools of the external project that you think can be adopted by your NUS-OSS project:

I honestly think that our issue tracker is very cluttered since it serves many purposes, other than issues regarding teammates itself. I think it might be better if we shift troubleshooting issues and self-introduction to slack channels instead. Of course, that would mean that we have to be responsive on slack so that new developers feel welcome. On that note, it is also extremely important to be friendly to new developers so that they will want to continue to work on the project.

SwiftLint allows autocorrection of style violations to be some extent. This feature would be especially useful if we can autocorrect whitespaces. SwiftLint is also run when the project is built, instead of being a separate static analysis on its own, which makes style errors easy to check and fix. 


## Suggested areas of improvement for the external project:

They can compile a list of issues faced during setting up, as well as how to fix them so that it is easier for new developers to troubleshoot.  While having a slack channel might be useful for such cases, I feel that a log of solutions would be better as sometimes the person who knows how to solve the problem might not always be available to answer.

It would also be good to have an architecural overview so that it is easier for new developers to navigate around the large codebase. 