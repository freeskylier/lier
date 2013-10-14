This is a collection of notes regarding security considerations in Lantern.  It is intended to be a resource for anyone wondering about how the different parts of Lantern are secured against potential threats.

### Certificate Exchange

Lantern proxies and clients mutually authenticate using client certificates.  These certificates are exchanged via XMPP messages between the client and the proxy sent through Google Talk.  In particular, here's the sequence:

 1. Proxy->Client: Send presence notification
 2. Client->Proxy: Here's my cert, send me yours
 3. Proxy->Client: Here's my cert

Certificates are immediately trusted upon receipt because the XMPP channel is trusted:

 * Both client and proxy are authenticated against Google Talk
 * In steps 2 and 3, certificates are delivered only if the users are on each other's rosters (i.e. at some point they authorized each other to chat)
 * If the users rejected a friend through the Lantern UI, the certificates are not trusted (even if they are on each other's rosters)

