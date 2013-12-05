Lantern will at times have multiple releases that are under more or less active development.  This branching strategy attempts to accommodate this.

For example, let's say that we have the following situation:

1.0 release is producing release candidates (1.0-rc1, 1.0-rc2, etc.)
1.0.1 (maintenance release) is being developed
1.1 (next minor or major release) is also being developed

* When development is ready to start on 1.1, a maintenance branch is created for the prior release (e.g. 1_0).
* Development for the next minor or major release (e.g. 1.1) happens on master.
* Bug fixes for the release candidate (1.0-rc*) are made directly on the maintenance branch (1_0)
* The maintenance branch is frequently (preferably right after each bug fix) merged into master
* Development of bugs/features for the maintenance release (1.0.1) are made in feature branches that will be merged into the maintenance_branch once the final 1.0 release has been cut.
* As soon as feature branches are merged into the maintenance branch, the maintenance branch is immediately merged into master