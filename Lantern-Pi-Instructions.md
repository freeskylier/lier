#  Lantern Pi Instructions

![](http://192.241.213.146/img/lantern_pi.png)

This guide offers instructions for setting up and connecting your new Raspberry-Pi powered Lantern. 

- Your Lantern goes perfect alongside your home router. Plug-in the ethernet cable (included with your kit) into an available port on your router. 
- Connect the power supply. You should see your device power on. After the boot processes finishes, a script to start the Lantern application is immediately executed. This is configured in /etc/rc.local.
- Open your current instance of Lantern on a home computer that's connected to the same local network. If you do not have Lantern installed already, you can download it from here: https://getlantern.org
- Once you have Lantern open, use the UI to pull up the Settings modal (it's accessible from a small gear icon in the lower right part of the UI screen). This window contains a "Local Lanterns" section, and the address for your Lantern should appear there as a clickable link. This will open the UI (a real-time world map) with statistics about your Lantern and the overall network. From here, you can adjust settings as you ordinarily would from your current instance. 
- To make sure your Lantern is able to proxy traffic (and you will know this is happening if the brightness of the light changes), you need a router with NAT-PMP or UPnP enabled, which automates the process of port forwarding. Another option is to manually map external port 443 to internal port 44377. Consult your router manual for more information.
- At any given moment, the luminosity of your lantern is measured by the average bandwidth being consumed; in other words, the more give-mode traffic you happen to be serving, the brighter the lantern becomes.
- If you would rather connect your Lantern using the included WiFi adapter, follow the instructions here: http://www.raspberrypi.org/documentation/configuration/wireless/

# Troubleshooting
- If it does not appear there, and you are familiar with a shell, you can use nmap to locate the device:
```  
nmap -sn 192.168.1.0/24
```