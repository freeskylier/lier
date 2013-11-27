Currently packaged installation on Linux is only available on Ubuntu. Contributions for other Linux distros and improvements to make better use of package managers are much appreciated. Other distros can also always [build from source](https://github.com/getlantern/lantern/blob/master/README.md#setting-up-a-development-environment).

The invitation to lantern has a link to an installation script. This script:

  + Downloads a .deb file.
  + Creates the uninstall script in /opt/lantern-net-installer,
  + Creates a user preferences directory (where, BTW, 'cause ~/.lantern
    doesn't seem to appear until first launch?), and
  + Does _not_ auto-launch a lantern service; 

### Installation

  1. Click the link named "Ubuntu 12.04+" in the installer. A new tab should open telling you a download should begin.
  2. A popup should appear, asking you to save a file named "lantern-net-installer_unix.sh". Download the file.
  ![download popup](http://i.imgur.com/justLyz.png)
  3. Open up a new instance of the terminal by clicking the Ubuntu button on the main menu bar of Ubuntu and typing "terminal".
  4. Click on the "terminal" icon to launch a new instance.
  ![finding terminal](http://i.imgur.com/AGo6Hve.png)
  5. Change to the directory where you downloaded the file from the browser:
    + `cd Downloads/`
  6. Make the install script executable:
    + `chmod 700 lantern-net-installer_unix.sh`
  7. Execute the install script:
    + `sudo ./lantern-net-installer_unix.sh`
    + Note: if you receive a message regarding no suitable Java Virtual Machine, you need to download Java.
      + See https://help.ubuntu.com/community/Java if you need help completing this.
running install script
  8. A message should appear saying that the installer is starting and a popup should appear titled "Lantern Fetcher". Wait while the fetcher fetches the Lantern program.
  ![installing](http://i.imgur.com/S2hBiEY.png)
  9. The installer will finish and give no message.
  10. Open up the Lantern program by clicking the Ubuntu button on the main menu bar of Ubuntu and typing "lantern".
  11. Click on the "Lantern" icon to launch the program.
    + Note: if you receive a message regarding Chrome not being installed, you need to download Chrome.
      + See https://www.google.com/intl/en/chrome/browser/ if you need help completing this.
![running lantern](http://i.imgur.com/pbBc1Rg.png)
  12. Wait while Lantern starts up.
  ![waiting for lantern to load](http://i.imgur.com/6m3gh25.png)
  13.  Welcome to Lantern!
  ![welcome to lantern](http://i.imgur.com/nnXoFjr.png)

After you've run the installer the next step is to [[Setup]] Lantern.

### Uninstallation

  1. Change directories to "/usr/local/lantern-net-installer/"
    + `cd /usr/local/lantern-net-installer/`
  2. Run the uninstall program.
    + `sudo ./uninstall`
    + ![run uninstall script](http://i.imgur.com/PW3hiCF.png)
  3. A window should popup.  Click "Next >" to continue uninstallation.
  ![uninstall program](http://i.imgur.com/PuEPZrB.png)
  4. The uninstall process should begin.  When finished, click "Finish".
  ![uninstall complete](http://i.imgur.com/7XZayjD.png)

