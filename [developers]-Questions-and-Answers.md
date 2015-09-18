# Questions and Answers

### Where can I learn more details about the Lantern architecture?

Check out our [developers' README](https://github.com/getlantern/lantern/blob/valencia/README-dev.md).


### <a name="other-circumvention-tools"/> Does Lantern work with other circumvention tools?

Running Lantern in Get Access mode may not work with other tools such as VPN software running at the same time. However, it should have no problem running at the same time as tools like the Tor Browser Bundle, which only affect their own connectivity, rather than all programs running on the computer. By default, Lantern in Get Access mode sets itself as your system proxy, so that all browsers running on the system will just use it automatically. So this is incompatible with other tools that expect to modify system-wide connectivity too. Lantern can be configured to not set itself as the system proxy (requiring you to specifically configure your browser to use it) under advanced settings.

### <a name="encryption"/> What type of encryption does Lantern use?

Lantern uses the following cipher suite for all connections between peers: TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA. That is, we use elliptical curve because of its shorter key lengths along with ephemeral Diffie-Hellman key exchange to preserve forward secrecy. We then use AES 256 in CBC block cipher mode instead of stream ciphers such as RC4 due to the greater number of known attacks on RC4. 

### <a name="certificates"/> What about certificates? Isn't Lantern vulnerable to man-in-the-middle attacks, especially with forged signing certificates from compromised certificate authorities?

First, Lantern connects to Google Talk servers over TLS. Lantern embeds the Google Talk signing certificate in its install and only trusts that certificate and a handful of others as trusted certificates, a sort of hard-coded form of certificate pinning. Lantern's connections between peers use self-signed certificates that are exchanged over XMPP through that trusted Google Talk connection. Lantern then only allows connections with those trusted certificates, thwarting any possible man-in-the-middle attack.

### <a name="kscope"/> How does Lantern distribute information about proxies?
Lantern uses an algorithm called Kaleidoscope to distribute information about p2p proxies. More information is available at Lantern's separate Kaleidoscope library implementation [here](https://github.com/getlantern/kaleidoscope). The core idea behind Kaleidoscope is to distribute information through a trust network in a limited manner such that no single actor on the trust network can enumerate all information distributed even if the trust network is compromised.

### <a name="performance"/> How will running Lantern affect performance on my computer?

Lantern's goal is to be as lightweight and unobtrusive as possible. In Get Access
mode, besides being able to access previously blocked sites, you shouldn't even notice it's running. In Give
Access mode, a portion of your internet connection will be
intermittently donated to other users, but based on the other users online
at the time, you may not even notice. We plan to intelligently limit the
resources Lantern consumes while you're using your computer in the future (see
[#19](https://github.com/getlantern/lantern/issues/19)).

### <a name="contributing"/> How can I contribute?

Please see the [[Contributing]] page.