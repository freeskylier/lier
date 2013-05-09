## Basic Get Mode test script

Before running this script, you can add the following to your /etc/hosts file to simulate Google being blocked:

```
0.0.0.0 talk.google.com
0.0.0.0 accounts.google.com
```

The test script should still succeed as long as Lantern can reach a fallback proxy.

1. Make sure Lantern is not running
1. Open up your system proxy settings and verify that you have no system proxy set. If your OS keeps this window up-to-date with your system proxy settings without your having to close and reopen it (OS X does, Ubuntu doesn't, afaik), keep this window visible while you interact with Lantern in the following steps so you can see exactly if and when Lantern changes the settings.
1. Nuke your ~/.lantern directory if you have one
1. Start up Lantern
1. Choose Give Access
1. Choose Sign In
1. Sign in to Google with an invited account and click Allow access
1. Click Continue (on the Lantern Friends modal)
1. Click Finish
1. Verify your green dot is in an accurate spot on the map, and when you hover over it all your details (including IP address) are accurate
1. Visit whatismyip.com in a browser
1. Verify your public IP is the same as in step 10
1. Click Settings button (gear icon)
1. Click Get Access
1. You should be taken to the Proxied Sites modal. Click Continue (should be "Continue" and not "Close" if setupComplete was correctly set back to false)
1. You should be taken to the System Proxy modal. Click Continue.
1. Check your system proxy settings are now configured to use Lantern's PAC file.
1. Back in Lantern, you should have been taken back to the visualization. Your dot should now be orange. When you hover over it, your details should be the same as before (including IP address).
1. You should now see a dark green dot corresponding to your fallback proxy. Hover over it and make a note of its IP.
1. Reload whatismyip.com, and see that an arc is drawn connecting your orange dot to the green dot.
1. Verify the IP that whatismyip.com is showing is now that of the fallback proxy.
1. Click Proxied Sites button (web icon)
1. Add geoiptool.com to the textarea and click Continue
1. Visit geoiptool.com and verify the IP and location it shows for you are the same as the fallback proxy's and not your orange dot's.
1. Quit Lantern
1. Check your system proxy settings now have no proxy set
1. Repeat steps 11-12
1. Restart Lantern
1. Check your system proxy settings now have Lantern's pac file set
1. Repeat steps 20-21 and then step 24
1. Go back to Settings and click Reset
1. Repeat steps 5-12