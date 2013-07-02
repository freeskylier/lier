This document outlines general coding guidelines for programmers working on the Lantern code base:

1. Master should always be stable enough to release at any moment.
1. Development should take place on branches
1. Each branch should be associated with one ticket or in rare cases several closely related tickets. If there are several closely related tickets, the branch creator should strongly consider consolidating the tickets into one.
1. Branches should be merged to master should be through pull requests
1. If any client-side change depends on a server-side change, branches for the lantern controller should be merged at the same time as client-side branches. See rule #1.
1. All code should be tested thoroughly through both unit tests and manual tests as appropriate.
1. Client side changes potentially affecting raw functionality should always be checked with our QA script before being merged.
1. Any more complicated changes should be tested on multiple operating systems.
1. All tests should pass always.
1. If you make changes that break the tests, you should fix the tests. Don't expect someone else will fix them.