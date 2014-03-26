Make sure that you've run the Lantern client and authenticated against Google to properly initialize your ~/.lantern folder.

Make sure that the <version> in your pom is correct and ends in -SNAPSHOT (e.g. 1.3.0-beta1-SNAPSHOT).

```
./release.bash
```

That will create a lantern-1.3.0-beta1 tag you can release from any time thereafter. To build the OSX installer for the above release, simply run:

```
./osxInstall.bash 1.3.0-beta1 true
```

You can also build an installer from the current HEAD without releasing (a throwaway installer for testing, for example) with the following:

```
./osxInstall.bash HEAD false
```

In that case you would **not use release.bash at all**.

If you just want to build an installer from what you have in your local environment, use `local` like this:

```
./osxInstall.bash local false
```

For the quickest build, you can build an installer from whatever maven build has already run by using 'quick':

```
./osxInstall.bash quick false
```