This document outlines general coding guidelines for programmers working on the Lantern code base:

1. All actual releases take place from the master branch. With each release, changes from devel are merged to master.
1. Devel should always be stable enough to release at any moment.
1. Development should take place on feature branches that are merged into the devel branch or the beta channel branch as appropriate.
1. Each branch should be associated with one ticket or in rare cases several closely related tickets. If there are several closely related tickets, the branch creator should strongly consider consolidating the tickets into one.
1. Feature branches should be merged to devel or the beta channel branch through pull requests.
1. Each pull request should be code reviewed
1. The original coder should also QA the fix.
1. The code reviewer should both review the code and QA the change.
1. The code reviewer should always be the one who actually does the merge.
1. If a PR is for a project outside of Lantern that requires new binaries in Lantern, those binaries should be integrated and committed as a part of the code review process.
1. If any client-side change depends on a server-side change, branches for the lantern controller should be merged at the same time as client-side branches. See rule #1.
1. All code should be tested thoroughly through both unit tests and manual tests as appropriate.
1. All tests should pass always.
1. If you make changes that break the tests, you should fix the tests. Don't expect someone else will fix them.