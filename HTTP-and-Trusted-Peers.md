HTTP and Trusted Peers
======================

When you select peers you trust using Lantern, you should know what exact behavior you're trusting. Lantern treats trusted peers specially. As described in [[HTTPS and Anonymous Peers]], Lantern always tries to send your requests through HTTPS versions of sites where all of your traffic is encrypted. In some cases, however, HTTPS versions of web sites don't exist, or Lantern doesn't know about them. In those cases, Lantern will send those request to your trusted peers and in some cases to [[Lantern Cloud Proxies]].

Why is this important? HTTP versions of sites are in plain text, so any shrewd entity with enough resources can read traffic sent over HTTP. Lantern encrypts the traffic between your computer and your trusted peers, but to access the ultimate web site you're trying to reach, the trusted peer must decrypt that traffic before forwarding it. So your trusted peer can theoretically read your traffic. This is why **you should only choose trusted peers you really trust**. It is also why **you should use HTTPS versions of web sites whenever possible**.
