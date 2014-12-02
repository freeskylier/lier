#Coding Guidelines

This document outlines general coding guidelines for programmers working on the Lantern code base:

##Branches
1. In general all work should take place on **feature branches**. In many cases those branch names will correspond with the number of the actual ticket. Depending on the feature, those branches will be merged into **either the devel branch or the beta branch**, with the beta branch typically containing more significant changes that will be merged into the main Lantern version within approximately three months. Stable releases are made from the master branch with a merge from devel prior to each release.
1. The devel branch, and correspondingly master, should always be stable enough to release at any moment.

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
1. If any client-side change depends on another module, including a server-side change, branches for the other module and/or binaries should be merged at the same time as client-side branches.

##Tests
1. All tests should pass always.
1. If you make changes that break the tests, you should fix the tests. Don't expect someone else will fix them.

##Happy Coding!!