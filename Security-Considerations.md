This is a collection of notes regarding security considerations in Lantern.  It is intended to be a resource for anyone wondering about how the different parts of Lantern are secured against potential threats.

### Peer Discovery

In order to start proxying requests through a Lantern proxy, a client has to first discover that proxy.  Discovery happens through an advertising process based on the [Kaleidoscope](https://github.com/getlantern/kaleidoscope) limited advertising protocol.

In particular, a Lantern proxy advertises itself as follows:

  1. Tell all its immediate Lantern friends about it (these are people whom the Give mode user explicitly added as a friend).  In particular, it's telling them:
     * The exact JID of the Lantern instance (assigned by Google Talk on startup of Lantern)
     * The ip address of the instance, both on its own LAN and as seen on the internet
     * If it was able to map a port using UPnP or NAT-PMP, the mapped port
  2. Each of these friends forwards this advertisement to a subset of their Lantern friends     
  3. Step 2 is repeated out to 4 levels

### Certificate Exchange

Lantern proxies and clients mutually authenticate using client certificates.  These certificates are exchanged via XMPP messages between the client and the proxy sent through Google Talk.  The exchange happens as a result of the client becoming aware of the server through the Kaleidoscope advertising process (see above).

One the client becomes aware of a proxy, the client sends that proxy its own certificate via a direct XMPP message.  Note - we do not relay this message through the chain of friends that advertised the proxy because that would require all of them to be online at the time that the client wants to access the internet.

When the proxy receives the client's certificate, it implicitly trusts it.  This is because the only way that Google Talk's XMPP server will deliver the message is if either:
  
  1. The peer sent the message to the exact JID for the running Lantern instance (e.g. email@company.com/23432adf), which is only made available through the Kaleidoscope discovery process
  2. The users are on already each other's rosters, meaning that the proxy's user at some point explicitly authorized the client to chat with him/her on Google Talk

In addition to trusting the client's certificate, the proxy immediately sends its certificate to the client via XMPP.  The client implicitly trusts the proxy's certificate for the same reasons that the proxy trusted the client's.

On both ends, if the user explicitly rejected the other user as a Lantern friend, the certificate received via XMPP will not be trusted.