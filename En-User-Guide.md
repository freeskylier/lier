# User Guide

## <a name="intro"/> Introduction

...

## <a name="installation"/> Installation

### <a name="installation-mac"/> Mac

Lantern is compatible with Mac OS X version 10.5 (Leopard) or higher. It's
a good idea to run the Apple Software Update app before installing Lantern to
make sure your system has all the updates available, which can include critical
stability and security updates.

After downloading Lantern, you will end up with a file that looks like
Lantern-0.XYZ.dmg. When you open this you will see a file called **Lantern
Installer**, which you can run to start the install process. If you already
have a previous version of Lantern installed on your computer, it will be
replaced with the new version. The installer will show its progress as it
copies files. When it's finished, Lantern will be started automatically and you
will be greeted with the welcome screen.


### <a name="installation-win"/> Windows

...

### <a name="installation-linux"/> Linux

...

## <a name="first-run"/> Running Lantern for the first time

### <a name="give-mode-and-get-mode"/> Giving vs. Getting Access

...

#### <a name="give-mode"/> Give Mode

...

#### <a name="get-mode"/> Get Mode

...

##### <a name="trusted-peers"/> Trusted Peers

Lantern treats trusted peers specially. Lantern always tries to send your
requests through HTTPS versions of sites where all of your traffic is
encrypted. In some cases, however, HTTPS versions of web sites don't exist.  In
those cases, Lantern will send those requests through your trusted peers or
through [Lantern Cloud Proxies](#wiki-cloud-proxies).

Why is this important? Content served over HTTP is sent unencrypted, so an
intermediary could potentially read the traffic as it passed through. Lantern
encrypts the traffic between your computer and your trusted peers, but to
access the ultimate web site you're trying to reach, the trusted peer must
decrypt that traffic before forwarding it. So your trusted peer can
theoretically read your traffic. This is why **you should only choose trusted
peers you really trust**. It is also why **you should use HTTPS versions of
web sites whenever possible**.

###### <a name="https-traffic"/> HTTPS Traffic

When you access a site over HTTPS, you access that site over an encrypted
connection that prying eyes cannot read. HTTP on the other hand, does not hide
your traffic in any way. Many web sites have both an HTTP and an HTTPS version,
and Lantern attempts to use the HTTPS version whenever possible. This happens
only in [Get Mode](#wiki-get-mode), although it may be enabled in [Give
Mode](#wiki-give-mode) in the future.

This system protects you, but it also has another property that's crucial to
Lantern's high performance architecture. Because your HTTPS traffic is
encrypted, Lantern sends that traffic through anonymous Lantern peers -- peers
you haven't explicitly trusted. There are several reasons for this. First,
because your traffic is encrypted, that peer cannot read the contents even
though they're passing through his or her computer. Second, at any given time
there are likely to be far more peers on the network who you don't know and
trust than there are peers who you do know and trust. If Lantern did not use
those peers you don't know, it would not be taking advantage of their
potentially huge computing power. Through using those anonymous peers, Lantern
is able to maximize performance for users in get access mode, taking more
efficient advantage of all the resources on the Lantern network.

**One important note** about this system, however, is that even though those
anonymous peers cannot read the contents of your traffic, **they can know the
IP address you are connecting with and the destination site you are going to**.
To illustrate this further, imagine you want to post to Twitter using Lantern.
If a government entity is running an anonymous peer that you happened to go
through, they would be able to tell your IP address and that you posted
something to Twitter at such and such a time. They would not know the contents
of that message, but they would know the site you visited, the time you
visited, and the size of the message you sent. In some cases that may even be
enough information to deduce that you sent a specific Tweet, although it might
be difficult to prove.

###### <a name="cloud-proxies"/> Lantern Cloud Proxies

Lantern Cloud Proxies are useful when you don't have any trusted peers online
with uncensored connections you can use. In that case, Lantern Cloud Proxies
act as a backup, available to proxy your traffic 24/7.

Lantern takes the responsibility of proxying your traffic very seriously. We
have an explicit interest in keeping any personally identifiable information
about the traffic routed through them secret and ephemeral, i.e. not stored,
analyzed, or shared with anyone. Any human contact with traffic information is
limited to only the core Lantern developers and is strictly incidental to
making sure Lantern works.

##### <a name="system-proxy"/> System Proxy

...

###### <a name="manual-proxy"/> Manual Proxy Configuration

Mac: System Preferences -> Network -> Advanced -> Proxies.
Select "Web Proxy (HTTP)" and then enter 127.0.0.1 for the server and
whatever port is set in your Lantern Dashboard in the [Settings
panel](#dashboard-settings).

## <a name="dashboard"/> Lantern Dashboard

### <a name="dashboard-status"/> Status

...

### <a name="dashboard-contact"/> Contact

...

### <a name="dashboard-settings"/> Settings

...

### <a name="dashboard-update"/> Update

...

## <a name="loop"/> Staying in the Loop

[Newsletter](http://getlantern.us2.list-manage.com/subscribe?u=0ac18298d5d0330dcda8f48aa&id=22c546d075)


## <a name="further-reference"/> Further Reference

- [Glossary](En-Glossary)
