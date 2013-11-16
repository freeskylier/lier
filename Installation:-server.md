To run Lantern on a server (like EC2 or another server you have access to), you will want to run it without the user interface. 

The way to do that right now is to [build from source](https://github.com/getlantern/lantern/blob/master/README.md#setting-up-a-development-environment) and run with `--disable-ui`.

Since there is no GUI you need some other way to tell the client who you are.  You do this by copying the following files to your EC2 machine:

https://github.com/getlantern/lantern/blob/master/src/main/resources/client_secrets_installed.json

(Which, contrary to its name, is not really a secret file), and

https://github.com/getlantern/lantern_aws/blob/master/salt/fallback_proxy/user_credentials.json

You need to edit the latter to substitute your email address for the {{ pillar['user'] }} string (that is, keep the double quotes, but replace everything inside them with your email).  You need to replace the entry that reads {{ pillar['refresh_token'] }} too.  The easiest way to obtain the "refresh token" you need to substitute there is to run the attached script (it needs Python 2 in your system).  You need to pass it the path to a local copy of the client_secrets_installed.json mentioned above, then follow instructions.

Once you have that, you run Lantern like this:

<path to lantern> --disable-ui --force-give --oauth2-client-secrets-file <path to your client secrets> --oauth2-user-credentials-file <path to your user credentials>

(--force-give is so it will run in give access mode.  That's the default as of this writing, but it can't hurt to pass it.)

Then you can use something like `screen` to leave Lantern running in the background.

As an alternative, if your EC2 instance runs Linux and you want to leave Lantern running as a service, and to be automatically launched on system startup, you may find this useful:

https://github.com/getlantern/lantern_aws/blob/master/salt/fallback_proxy/lantern.init

To use it,
 - edit line 21 to point to your Lantern executable.
 - edit line 22 to use only the arguments you set above.
 - copy the file to /etc/init.d/lantern
 - give it the right owner and permissions:
       sudo chown root:root /etc/init.d/lantern
       sudo chmod 700 /etc/init.d/lantern
 - start Lantern as a service.  In many Linux distributions you do this like so:
       sudo /etc/init.d/lantern start
   although in Ubuntu and some others you may also say
       sudo service lantern start

The headless interface doesn't currently provide a way to add friends, but you can do that through the graphical user interface in your home machine.