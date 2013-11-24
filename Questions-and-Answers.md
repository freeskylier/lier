### <a name="safe"/> Is Lantern safe for me to use?

Lantern takes great pains to ensure that users are safe, but there are cases we cannot protect against, so users need to be aware of how they can use Lantern safely. For users in censored regions itʼs extremely important that you only choose Lantern friends who you really trust. Your Internet traffic will run through those peers. If you add people who you donʼt trust, you run the risk of adding a user who could be monitoring you. So **only add Lantern friends that you really trust**. Beyond that, **Lantern will also send your traffic through peers up to four degrees away from you**, that is, friends of friends of friends of friends. We do this to build a more connected, scalable network, as users often don’t directly know anyone on the other side of the censorship divide. However, every additional link in the chain exposes you to a less and less trusted user (i.e. you trust your friends’ friends less than you trust your friends). Always keep in mind that **Lantern is a tool to provide access, it is not designed to prevent monitoring**.

**Lantern is not an anonymity tool**. If you require that the sites you visit do not learn your IP address or physical location (they normally can, which may come as a surprise), or you cannot risk network monitors being able to determine what sites you visit, we recommend you use [Tor](https://www.torproject.org). Tor is great software, and we communicate with the Tor team frequently. Again, Lantern’s purpose is access. Tor’s purpose is anonymity.

One last point on safety: With any tool, including both Lantern and Tor, you should never post sensitive content to a web site that is hosted in a region where the government pursues people who post such content, especially if you live there. This is because a global network observer like the government can identify you as the user who uploaded that content and will be able to geolocate you.


**Lantern is not designed to be an anonymity tool.** If you require that the websites you visit do not learn your physical location (they normally can, which may come as a surprise!) or you cannot risk network monitors being able to determine what web sites you visit, we recommend you use [Tor](https://www.torproject.org). Tor is great software, and we communicate with the Tor team frequently. Lantern is much more focused on access whereas Tor’s goal is anonymity.

One last point on safety: with any tool, including both Lantern and Tor, you should never post sensitive content to a web site that is hosted in your country if you live in a censoring region. The reason is simple: a global network observer, such as the government, will be able to identify you as the user who uploaded that content and will be able to geo-locate you. This is probably the most dangerous thing you could do, so make particularly sure you're posting to sites hosted outside of the country if you think that content could be controversial in some way.



### <a name="no-connections"/> How does Lantern work if I can't reach any users giving access?

To help get the Lantern network started we have set up [[Lantern Cloud Servers]]. These serve as fallbacks to proxy traffic when no other users are available to give access. Our hope is that as the Lantern network grows, there will be enough users giving access that we will need fewer and fewer fallback servers.

Our other plan is to give people an option to sponsor additional Lantern Cloud Servers dedicated for them and their friends. We also hope to partner with companies that have spare computing capacity and want to help internet freedom by donating servers to the Lantern network.


### <a name="compare"/>How does Lantern compare to other tools?

Lanternʼs goal is to give users access while being fast, secure, and easy to use. [Tor](https://www.torproject.org) is one of the most popular tools in this space with a primary focus on anonymity. For those who do not care about being completely anonymous, Lantern provides an alternative with typically faster access. Compared to other tools aimed at access (GoAgent, Freegate, Ultrasurf, Psiphon, Autoproxy) Lanternʼs strength is the ease with which it can be installed and used, as well as its trusted peer-to-peer network architecture designed to scale in the presence of censors. **The use of real-world trust relationships in Lantern also makes it extremely resilient to blocking attempts.**

By default, Lantern runs as a system proxy, which means that browsers on your computer will use it automatically, without your having to change any of their settings. Some other tools only work with one specific browser, or require complex configuration.

Another unique aspect in Lanternʼs design is its peer-to-peer architecture, which allows data to come from many computers at once, rather than a single server. Peer-to-peer architectures also allow networks to scale to millions of users at a fraction of the cost of more centralized architectures.

Recently, the Lantern team has contributed to [uProxy](https://uproxy.org), a new effort sponsored by Google Ideas. While there are similarities between the two, there are also some important differences. For one, Lantern is an independent app that stays running in the background, while uProxy is a browser extension, and currently requires asking a single friend to proxy for you on a per-session basis, so with Lantern you can have many peers give you access at the same time as opposed to just one. Another difference is Lantern allows friends of friends up to 4 degrees away to connect to one another, whereas uProxy only allows direct friends. Finally, to be faster and more blocking resistant, by default Lantern proxies access only to a specific set of sites you configure (see below), whereas uProxy reroutes traffic to all sites through your uProxy peer while you have it enabled.


### <a name="proxy-list"/> Why does Lantern not proxy every site by default? 

By default, Lantern only provides access to a list of known blocked sites. We do this for a couple of reasons. First, it is always faster to go to a site directly rather than through a proxy regardless of how fast or efficient that proxy is. So sites that arenʼt blocked will be fastest if they are reached directly instead of through Lantern.

The second reason is that not proxying access to sites that are known to be unblocked frees up Lantern network resources. Because the Lantern network as a whole doesn't have to carry the burden of providing access to unblocked sites, it can instead use those resources to provide you with better access to blocked sites.


###<a name="trust-network"/>How does the trust network work? What happens when I add someone as a Lantern friend?

Lantern is built on a trust network. This network connects people who trust one another to share internet connections. When you and another user are Lantern friends with one another, you can proxy traffic for one another using Lantern. However, if Lantern proxied only through direct friends, users would often have no proxies available whenever none of their direct friends were online giving access.

To mitigate this, Lantern users getting access can discover a subset of the users giving access up to 4 degrees away from them in the trust network. So for instance, if you use Lantern to get access, your brother’s partner’s mother’s friend could end up proxying your Lantern traffic. If this person is a censor, she could block or analyze your traffic. On the other hand, if you use Lantern to read or post something private or sensitive, it will look as though this traffic is coming from her computer. Because of this, everyone running Lantern should only friend people they trust, and **only use Lantern to proxy traffic that is not private or sensitive**.

By only adding people you trust, you protect not only yourself, but also your friends, their friends, their friendsʼ friends, and so on. And by allowing users to discover a subset of users farther away from them in the trust network, Lantern increases available proxies while maintaining blocking resistance.

In any scenario, however, **you have to explicitly approve each user who will proxy access for you**. You are always in control. Lantern will never send your traffic through any peer, regardless of how far away they are in the trust network, without your explicit approval.


### <a name="howto"/> How do I download Lantern?

Lantern is still in private beta. You can request an invitation and updates [here](https://getlantern.us2.list-manage.com/subscribe/post?u=0ac18298d5d0330dcda8f48aa&id=f06770f311).


### <a name="know"/> I live in an uncensored region and don't know anyone in a censored region. Can I still help?

Definitely! People in censored regions can still learn about you through your friends. So while you donʼt know anyone directly living in censored regions, your friends might, and the odds are even better that their friends might (and so on). If you keep Lantern running and adding the people you trust, eventually youʼll be connected with users who need access. **Thatʼs why itʼs really important to invite your friends to Lantern**. It maximizes the likelihood that your social network will reach into censored regions so you can help.

### <a name="gmail"/>Is a Gmail account required to use Lantern?
Yes. Lantern requires a Gmail or Google Apps e-mail address. For details, see [Why Does Lantern Require a Google Login?](https://github.com/getlantern/lantern/wiki/%5Bdevelopers%5D-Questions-and-Answers#-why-does-lantern-require-a-google-login-what-happens-with-the-generated-oauth-tokens).

### <a name="whattodo"/> OK, I've installed Lantern. Now what?

For users in uncensored regions, there are two basic things you can do once youʼve installed Lantern:

1. **Run Lantern as much as possible.**
1. **Add more users you trust as Lantern friends.**

Whenever you run Lantern, you create a new access point users in censored regions can use to access the open Internet. Remember, though, that only people in your Lantern network will be able to connect to you. Thatʼs why the second step is critical. The larger your Lantern network, the higher the odds youʼll provide access to users who need it. **So please invite as many trusted contacts as you can!**

### <a name="upgrade"/>How do I upgrade to a newer version of Lantern?

Please see [Upgrading to a New Version of Lantern](https://github.com/getlantern/lantern/wiki/Upgrading-to-a-New-Version-of-Lantern).

### <a name="hackers"/> Will Lantern make my computer vulnerable to hackers?

Lantern takes a number of precautions to make sure users are safe. First, Lantern does not allow anyone it connects you to to read the contents of your computer. It simply allows you to share Internet connections. The data passing between you is encrypted so that no intermediaries (e.g. your government or Internet service provider or theirs) can read it. Lantern also requires mutual authentication for all connections, which means that Lantern will only allow users to connect to you that it can verify are in your Lantern network, and not just anyone.


### <a name="is-lantern-free"/> Is Lantern free? Will running it cost me anything?

Lantern is free as in money and as in freedom: free to use, modify, and redistribute in accordance with its [license](https://raw.github.com/getlantern/lantern/master/LICENSE).

If your Internet connection is limited, then giving access through Lantern will count against your limit. We recommend using Lantern with unlimited Internet connections.


### <a name="contributing"/> How can I contribute?

Please see [[Getting Involved|Get-Involved]].

### <a name="notworking"/> Lantern's not working for me. What's up?

There is a known incompatibility between Lantern and Proxy Switchy. If you have Proxy Switchy installed, you can temporarily disable it to use Lantern.


### <a name="more"/> I have more questions, where do I go?

If you have more technical questions, please see the [Developers Q&A](https://github.com/getlantern/lantern/wiki/%5Bdevelopers%5D-Questions-and-Answers) page. Also feel free to post to the [user forums](https://groups.google.com/group/lantern-users-en) or the [develepors forum](https://groups.google.com/group/lantern-devel).