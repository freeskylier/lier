### Supported Versions

Lantern supports OS/X version 10.6 and higher, 64-bit only.

### Installation

![download lantern](https://www.evernote.com/shard/s209/sh/8f36ed28-7670-4213-8a2f-e971a8de59ca/88a3b4388faf0766d3a3521a874e1f01/deep/0/Lantern%20Invitation%20-%20cholmes@cartodb.com%20-%20CartoDB%20Mail.png)

Download Lantern from your invite email. This should download a file called `lantern-net-installer_mac_os_0_0_1.dmg`. This will be relatively small - approximately 1.5mb - as it fetches more needed files from the internet.

![install](https://www.evernote.com/shard/s209/sh/6b406cb3-6270-4117-ba61-d6a8e3281728/a04236b62b8daf0096ad2f6670c46696/deep/0/Menubar%20and%20lantern-net-inst%202%20and%20Applications.png)

Double-click on the .dmg file, and then double-click on the 'Lantern Installer' icon.

![downloading](https://www.evernote.com/shard/s209/sh/b39a5f0d-4aa9-4518-8a26-fd0a86de8737/9d3090f5eab319830f4510bc13bba90e/deep/0/Lantern%20Fetcher.png)

If you click on the .dmg and nothing happens the most likely problem is you are not an admin user.
As of beta2 this will _**not**_ work if you are not running as an admin user. We are [working](https://github.com/getlantern/lantern/issues/819) on getting it to prompt for the admin password instead of just failing. 

As long as you are an admin user clicking on the .dmg will do several things. It will detect if you have Java, and if not it will download the Java Runtime Environment from the web. Then it will download the latest Lantern code, to make sure your installation is totally up to date. If you are on a slow connection the download step may take a bit of time.

![install4j](https://www.evernote.com/shard/s209/sh/c92df454-472a-4ce1-a578-fc06843802d7/04fd633f4deb9fbeecc44562dff2ea78/deep/0/Screenshot%208/16/13%207:52%20PM.png)

Next you will get a prompt about 'install4g'. Install4g is a program we use to make the Lantern install experience smoother across all platforms, so just enter your password, as that is Lantern getting permission to install itself and to make changes to your proxy settings so your connection can be shared.

![extracting](https://www.evernote.com/shard/s209/sh/377e6ed3-ce38-480b-b79a-bd0d540ae375/84fc0a6e71cbe529d194a4461c8d82be/deep/0/Screen%20Shot%202013-08-16%20at%207.52.52%20PM.png)

This should extract files and then startup your lantern instance.

![lantern default](https://www.evernote.com/shard/s209/sh/57a422d3-27f1-4b45-b05c-09b87636ab23/8b8d1d84c456798cd0f3e045590dc3e7/deep/0/Lantern.png)

If you see this screen you're all set. Proceed to [[Setup]].

### Stopping Lantern

We encourage you to just leave Lantern running in the background, so it can be helping censored users get access even while you're doing other tasks. 

If you close the window a lantern icon will still stay in your menubar. To stop it entirely click on the lantern icon and select 'Quit Lantern'.

![quit lantern](https://www.evernote.com/shard/s209/sh/9308b039-b326-4160-b7d1-4f6f15c210a7/41fe4b0ebde601cb9ffd5d0ceb09a8c8/deep/0/Screen%20Shot%202013-08-16%20at%208.07.29%20PM.png)

### Uninstallation

To fully uninstall Lantern you must move the Lantern icon in the Applications folder to the Trash. You must stop Lantern before doing this. Doing this will also uninstall Lantern's Java Runtime Environment. You can also delete the '''.lantern/''' directory in your home directory. Doing this will prompt you for [[Setup]] if you ever reinstall lantern. If you leave it then Lantern will start working with your existing setup.