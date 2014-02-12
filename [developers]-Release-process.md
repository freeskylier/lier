After running through QA scripts, simply run the following for our example 0.21.3-1 release:

```
./release.bash 0.21.3-1 
```

That will create a 0.21.3-1 tag you can release from any time thereafter. To build the OSX installer for the above release, simply run:

```
./osxInstall.bash 0.21.3-1 true
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