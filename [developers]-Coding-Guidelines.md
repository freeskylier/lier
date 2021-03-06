#Coding Guidelines

This document outlines general coding guidelines for programmers working on the Lantern code base:

##Branches
1. We follow the branching strategy described in more detail [here](http://nvie.com/posts/a-successful-git-branching-model/)
1. In general all work should take place on **feature branches**. In most cases those branch names will correspond with the number of the actual ticket prepended with "issue-" to avoid potential conflicts with commit short codes (happens surprisingly often when ticket numbers get large apparently). Depending on the feature, those branches will be merged into **either the devel branch or the current release branch**, with the current release branch being reserved for changes going into updates to the current beta. As such, they should generally only contain more stable changes while more destabilizing changes should be merged to devel for inclusion in the subsequent, as yet unreleased beta version.

##Tickets
1. When initially creating tickets, specify the milestone, priority, and assignee if you feel you know them. Otherwise leave them blank and let the ticket wranglers handle that part.
1. All tickets we actually work on should have a milestone, a priority, and an assignee. If they don’t, and you feel you should start working on a ticket, either add them or contact the appropriate ticket wranglers.
When a ticket is fixed, add the “QA” label if it’s possible to test in QA, leave the ticket open, and assign it to @sunshine19090. Otherwise label it as “NOT TESTABLE IN QA” and close it.
1. All the issues moved to QA should be tested by Sunshine when the build is ready to test.
1. After testing, if the issue is not resolved then move it to REJECTED and assign it to the dev person to fix the issue. Follow step 2.
1. After testing, if the issue is resolved then close it.
1. If an issue is a duplicate, add duplicate label and close it.
1. If a issue is recurring, reopen the ticket and assign it to the dev person and follow step 2.
1. Before releasing, all the major tickets for that release should have been closed. If the ticket is decided to be of low importance at that moment, then move it to next release.

###Ticket Priorities
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
1. Each change should happen through a pull request (PR), and each pull request should be code reviewed
1. The code reviewer should both review the code and QA the change.
1. The code reviewer should always be the one who actually does the merge.
1. If a PR is for a project outside of Lantern that requires new binaries in Lantern, those binaries should be integrated and committed as a part of the code review process.
1. If any change depends on another module branches for the other module and/or binaries should be reviewed and merged at the same time as client-side branches.
1. When a merge is complete the feature branch **should be deleted** to avoid proliferation of branches.

## QA
1. For any ticket that is testable in QA, the final step in the ticket should be to assign it to QA for testing and ultimate closing. For those tickets for which this applies, this should be done after code review and merging. 
1. If there are any problems at the QA stage, the ticket should be re-assigned back to the original developer for additional work.

##Tests
1. All tests should pass always.
1. If you make changes that break the tests, you should fix the tests. Don't expect someone else will fix them.

##Happy Coding!!