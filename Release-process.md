After running through QA scripts, simply run the following for our example 0.21.3-1 release:

```
./release.bash 0.21.3-1 
```

That will create a 0.21.3-1 branch you can release from any time thereafter. To build the OSX installer for the above release, simply run:

```
./osxInstall.bash 0.21.3-1 true
``` 