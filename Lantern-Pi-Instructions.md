 Lantern Pi Instructions

![](http://192.241.213.146/img/lantern_pi.png)

This guide offers instructions for setting up and connecting your new Raspberry-Pi powered Lantern. 

- Your Lantern goes perfect alongside your home router. Plug-in your ethernet cable (included with the kit) into an available port on your router. 
- Connect the power supply. After the boot processes finishes, the Lantern application should immediately start running. 
- Open your current instance of Lantern on a home computer that's connected to the same local network. If you do not have Lantern installed already, you can download it from here: https://getlantern.org
- Open you have Lantern open, use the UI to access the Settings modal (it's accessible with a small gear icon in the lower right part of the UI screen). This window contains a "Local Lanterns" section, and the address for your Lantern should appear as a clickable link. This will open the UI (a current world map) of your Lantern. From here, you can adjust settings as you would ordinarily from your current instance. 
- To make sure your Lantern is able to proxy traffic (and you will know this is happening if the brightness of the light changes), you need a router with NAT-PMP or UPnP enabled, which automates the process of port forwarding. Another option is to manually map external port 443 to internal port 44377. Consult your router manual for more information.


Troubleshooting
- If it does not appear there, and you are familiar with a shell, you can use nmap to locate the device:
```  
nmap -sn 192.168.1.0/24
```