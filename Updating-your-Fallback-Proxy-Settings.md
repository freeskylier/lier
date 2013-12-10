If you are unable to connect to your fallback proxy but you learn about another fallback proxy, you can manually configure Lantern to use that fallback proxy.

To do this you need to find the fallback.json on your platform:

##### Windows Vista/7/8

`C:\Users\USERNAME\AppData\Roaming\Lantern\fallback.json`

##### Windows XP

`C:\Documents and Settings\USERNAME\Application Data\Lantern\fallback.json`

##### OSX 

`~/.lantern/fallback.json`

##### Ubuntu 

`~/.lantern/fallback.json`

Open the fallback.json file in a text editor.  It will look like this:

{    
    "ip" : "54.254.96.14",
    "port" : 16589
}

Change the ip and port to match whatever value you want, save the file and restart Lantern to pick up the change.

Note - when you install a new version of Lantern, your settings will get overwritten.