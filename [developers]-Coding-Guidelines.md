#Coding Guidelines

This document outlines general coding guidelines for programmers working on the Lantern code base:

##Branches
1. We follow the branching strategy described in more detail [here](http://nvie.com/posts/a-successful-git-branching-model/)
1. In general all work should take place on **feature branches**. In many cases those branch names will correspond with the number of the actual ticket. Depending on the feature, those branches will be merged into **either the devel branch or the current release branch**, with the current release branch being reserved for changes going into the next version. As such, they should generally only contain more stable changes while more destabilizing changes should be merged to devel for inclusion in the subsequent release.

##Priorities
Priorities are tracked as labels in GitHub. All issues in the short-term milestone should have priorities, and engineers should work on issues in order of priority as they see fit.

**P0** -- This is a severe issue in production that needs to be fixed right away.

**P1** -- We will consider ourselves abject failures if this is not included in the next release.

**P2** -- This an important feature for the next release.

**P3** -- A "nice to have" for the next release.


##Coding
Code on specific features and/or bugs should include the following:

1. A corresponding ticket
1. Unit tests
1. Reasonable code coverage
1. End to end testing of the change
1. A pull request
1. End to end testing of the feature, including integrating new binaries into Lantern if necessary

##Code Reviews
1. Each pull request should be code reviewed
1. The code reviewer should both review the code and QA the change.
1. The code reviewer should always be the one who actually does the merge.
1. If a PR is for a project outside of Lantern that requires new binaries in Lantern, those binaries should be integrated and committed as a part of the code review process.
1. If any change depends on another module branches for the other module and/or binaries should be reviewed and merged at the same time as client-side branches.
1. When a merge is complete the feature branch should be deleted to avoid proliferation of branches.

##Tests
1. All tests should pass always.
1. If you make changes that break the tests, you should fix the tests. Don't expect someone else will fix them.

##Happy Coding!!