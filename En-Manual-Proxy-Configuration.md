# Manual Proxy Configuration

By default, Lantern automatically configures your computer to use Lantern as
a local HTTP proxy **when you are running in get access mode.** When you are
running in give access mode, Lantern does not modify your proxy settings in any
way.

If you would prefer to manually set your proxy settings, however, you can do so
in the Lantern Dashboard "Settings" panel. First, select "Open Dashboard" from
the Lantern menu item on OSX (top bar on your screen) or the system tray on
Windows (icons at the lower right). Then select "Settings" and uncheck the
checkbox for using Lantern as the system proxy. 

If you do this, you then have to manually configure your proxy settings if you
want to use Lantern.

On OSX, this is under System Preferences->Network->Advanced->Proxies. The
easiest way to change them is to select "Web Proxy (HTTP)" and then enter
127.0.0.1 for the server and whatever port is set in your Lantern Dashboard in
the Under the Hood panel.
