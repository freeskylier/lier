# HTTPS and Anonymous Peers

When you access a site over HTTPS, you access that site over an encrypted
connection that prying eyes cannot read. HTTP on the other hand, does not hide
your traffic in any way. Many web sites have both an HTTP and an HTTPS version,
and Lantern attempts to use the HTTPS version whenever possible. This happens
only in get access mode, although we may enable it for give access mode in the
future.

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