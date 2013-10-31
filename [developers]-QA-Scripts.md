## Basic Get Mode test script

The test script should still succeed as long as Lantern can reach a fallback proxy. When we switch to give mode about halfway through the script, you'll enter the following in your /etc/hosts file:

```
0.0.0.0 talk.google.com
0.0.0.0 accounts.google.com
0.0.0.0 google.com
```

Alternately, if you have access to a firewall, you can block the below ip ranges

```
216.239.32.1 - 216.239.63.254
54.233.160.1 - 54.233.191.254
66.249.80.1 - 66.249.95.254
72.14.192.1 - 72.14.255.254
209.85.128.1 - 209.85.255.254
74.125.0.1 - 74.125.255.254
207.126.144.1 - 207.126.159.254
```

Note - these will change over time.  Up to date ranges can be obtained by calling `dig @ns1.google.com -t txt _netblocks.google.com` and converting the resulting _netblocks to ip ranges using this [online ip calculator](http://jodies.de/ipcalc).

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
1. **We're now going go switch to get access mode**. Add the google mappings above to your /etc/hosts file to simulate Google being blocked (see beginning)
1. Click Settings button (gear icon)
1. Click Get Access
1. You should be taken to the Proxied Sites modal. Click Continue (should be "Continue" and not "Close" if setupComplete was correctly set back to false)
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


**Also Test:**
- autostart on system startup
- p2p