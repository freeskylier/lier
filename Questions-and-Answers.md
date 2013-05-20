# Questions and Answers

### <a name="encryption"/> What type of encryption does Lantern use?

Lantern uses the following cipher suite for all connections between peers: TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA. That is, we use elliptical curve because of its shorter key lengths along with ephemeral Diffie-Hellman key exchange to preserve forward secrecy. We then use AES 256 in CBC block cipher mode instead of stream ciphers such as RC4 due to the greater number of known attacks on RC4. 

### <a name="certificates"/> What about certificates? Isn't Lantern vulnerable to man-in-the-middle attacks, especially with forges signing certificates from compromised certificate authorities?

First, Lantern connects to Google Talk servers over TLS. Lantern embeds the Google Talk signing certificate in its install and only trusts that certificate and a handful of others as trusted certificates, a sort of hard-coded form of certificate pinning. Lantern's connections between peers use self-signed certificates that are exchanged over XMPP through that trusted Google Talk connection. Lantern then only allows connections with those trusted certificates, thwarting any possible man-in-the-middle attack.

### <a name="google"/> Why does Lantern require a Google login? What happens with the generated OAuth tokens?

Lantern require's users to login to Google Talk for the following reasons:

1. It allows you to easily connect with your existing Google Talk contacts via Lantern in order to bootstrap the trust network
2. It allows Lantern to use Google's XMPP servers to negotiate direct P2P connections between users
3. Google Talk is also largely unblocked, so it provides a channel through which Lantern can usually communicate

When you login to Google via OAuth, Lantern stores your OAuth refresh token on your local computer in an encrypted form using your operating system's keychain, or an equivalent if your operating system does not support a keychain.

### <a name="hackers"/> Will Lantern make my computer vulnerable to hackers?
Lantern takes a number of precautions to make sure users are safe. First, Lantern does not allow any external computers to access your hard drive. Instead, Lantern simply acts as a conduit for your trusted contacts, relaying their requests to web pages on the open Internet as well as the replies from those web pages. External users have no access to your computer itself. Lantern also requires what's called mutual authentication for all connections, requiring that anyone connecting through you to the open Internet is someone you have a cryptographic key for, so someone who has learned about your computer through either being a trusted contact directly or through one of your trusted contacts. This ensures that random computers out there cannot use your computer as an access point to the open Internet.

### <a name="performance"/> How will running Lantern affect performance on my computer?

Lantern's goal is to be as lightweight and unobtrusive as possible. In [Get
Mode](En-User-Guide#wiki-get-mode), you shouldn't even notice it's running,
outside of being able to access previously blocked sites of course. In [Give
Mode](En-User-Guide#wiki-give-mode), a portion of your internet connection may
intermittently be donated to other users, but based on the other users online
at the time, you may not even notice. We plan to intelligently limit the
resources Lantern consumes while you're using your computer in the future (see
[#19](https://github.com/getlantern/lantern/issues/19)).


### <a name="is-lantern-free"/> Is Lantern free?

Lantern is free as in money and as in freedom: free to use, modify, and
redistribute in accordance with its
[license](https://raw.github.com/getlantern/lantern/master/LICENSE). This
documentation is likewise distributed under a [[free license|LICENSE.txt]].


### <a name="contributing"/> How can I contribute?

Please see the [[Contributing]] page.