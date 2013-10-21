### <a name="safe"/> Is Lantern safe for me to use?

Lantern takes great pains to ensure that users are safe, but there are cases we cannot protect against, so users need to be aware of how they can use Lantern safely. 

For users in censored regions it's extremely important that you only choose Lantern friends who you really trust. By only adding people you trust to your list of friends, you **reduce the risk of being monitored but you do not eliminate it entirely.** Your Internet traffic will run through those peers. If you add people who you don't trust, you run the risk of adding a user who could be monitoring you.**Only add Lantern friends who you really trust**. Adding more friends will make Lantern perform better, but they need to be trusted friends.

**Lantern is not designed to be an anonymity tool**. If you require that the websites you visit do not learn your physical location (they normally can, which may come as a surprise!) or you cannot risk network monitors being able to determine what web sites you visit, we recommend you use [Tor](https://www.torproject.org). Tor is great software, and we communicate with the Tor team frequently. Lantern is much more focused on access and usability, and Tor does a much better job with anonymity.

One last point on safety: with any tool, including both Lantern and Tor, you should never post sensitive content to a web site that is hosted in your country if you live in a censoring region. The reason is simple: a global network observer, such as the government, will be able to identify you as the user who uploaded that content and will be able to geo-locate you. This is probably the most dangerous thing you could do, so make particularly sure you're posting to sites hosted outside of the country if you think that content could be controversial in some way.

For give mode users, Lantern doesn't compromise your personal information and data. It works in the background and it shouldn't effect your operating system speed.  

### <a name="no-connections"/> How does Lantern work if I can't reach any users giving access?

To help get the Lantern network started we have set up '[[Lantern Cloud Servers]]'. These are dedicated servers that serve as a 'fallback' to proxy user traffic if no one else is available. Users with no connections will make use of these. We know this approach is not scalable, as it would end up costing tons of money. Lantern is built with a unique algorithm that lets you make use of connections of friends of friends, up to four 'hops' away - friends of friends of friends of friends. Our hope is that the social network grows dense enough that there is very little load on the fallback servers. When there gets to be too many people we will likely throttle the connections, so that people who do make good connections get faster access.

Our other plan is to give people an option to buy or donate additional Lantern Cloud Servers. People in censored countries who know no one outside, or just want a reliable connection, could sponsor a server for just themselves or their friends. We hope to eventually let people sign up for free servers like Google App Engine as well. We also hope to partner with companies that have spare computing capacity and want to help internet freedom by donating virtual servers to run Lantern and add more Lantern Cloud Servers to the pool.

### <a name="compare"/>How does Lantern compare to other tools?

Lantern's main focus is access, with a big emphasis on usability. Tor is one of the most popular tools in this space, but their primary focus is anonymity. Because of this, Tor can be relatively slow to surf the web. For those who do not care about being completely anonymous, Lantern provides an alternative with faster access. Compared to the other tools aimed at access (GoAgent, Freegate, Ultrasurf, Psiphon, Autoproxy) Lantern's strength is the ease with which it can be installed and used. It is designed to just work without having to understand what a proxy is. 

Lantern is also a bit different in that it runs as a system proxy, meaning any program you run will automatically use the proxy. Other programs will only work with the browser, or take complex configuration. Since Lantern adjusts the core system every program works more naturally. Lantern also only proxies the sites that you configure it for, so sites that are not blocked are not run through the proxy. VPN's and others just run your traffic through indiscriminately. 

The other unique thing about Lantern is its peer-to-peer approach, which makes downloading faster because data comes from many computers at once, not just one server. This also makes it so it can eventually handle millions of users without costing a fortune, since it just needs spare bandwidth from any computer, instead of specialized servers running.

Recently, the Lantern team has been contributing to UProxy, a new effort sponsored by Google Ideas. While there are similarities in the P2P approach, Lantern is a separate software program that runs in the background. The plan for UProxy is for it to work as a browser extension. 

<a name="proxy-list"/> Why does Lantern not proxy every site by default? 

Lantern relies on its configured proxied site list for a couple reasons. One is efficiency. Though Lantern is designed to be fast it is always more faster to go to the site directly than to go through a proxy, or even a bunch of peer proxies. So sites that aren't blocked will be fastest if they are reached directly instead of through Lantern. 

The second is that it potentially helps mask the traffic more. Instead of seeing a user always connect to a handful of special locations (users in their Lantern network giving access), a censor will see them accessing sites that aren't blocked directly, the same patterns as when they aren't running Lantern. So proxying only what is blocked helps that traffic 'blend in' with everything a user is doing.

###<a name="trust-network"/>How does this 'trust network' work? What happens when I add someone as a Lantern friend?

Adding someone as a friend in Lantern means that the two of you will share an internet connection. The user in 'get mode' - in a censored country - will trust their friend to flow internet traffic through their computer. A stranger could potentially analyze that traffic and use it for harm, so you should only become Lantern friends with people you actually know. On the flip side the user in 'give mode' trusts that their Lantern friend is not using their connection to do anything illegal, like download child pornography, as the traffic the user in a censored country generates will show up as their own traffic.

These individual connections of trust build up a full network of trust, where users can proxy not just through friends, but through friends of friends. This trust network also makes Lantern much more resistant to censorship blocking techniques than other approaches.

### <a name="resist-blocking"/>How does the trust network make Lantern resistant to blocking?

(TODO)


### <a name="howto"/> How do I download Lantern?
Lantern is still in development. We are currently accepting applications to become Lantern Ambassador beta testers. You can sign up to be one of our first beta testers by filling out this survey:  [Lantern Ambassador Questionnaire](https://docs.google.com/forms/d/11LiZoCMptcc_lj4b01It9n64gngaDPU53_ge3mhiaIM/viewform), and visit [https://www.getlantern.org](https://www.getlantern.org) to sign up for our mailing list.

### <a name="know"/> I live in an uncensored region and don't know anyone in a censored region. Can I still help?
Definitely! People in censored regions can still learn about you through your friends. So while you don't know anyone directly living in censored regions, your friends might, and they'll relay your information to their trusted friends in censored regions. **That's why it's really important to invite your friends to Lantern.** It maximizes the likelihood that your social network will reach into censored regions so you can actually help!


### <a name="whattodo"/> OK, I've installed Lantern. Now what?
For users in uncensored regions, there are two basic things you can do once you've installed Lantern:

1. **Run Lantern as much as possible**
1. **Invite more users**

Whenever you run Lantern, you create a new access point users in censored regions can use to access the open Internet. Remember, though, not everyone can access the Internet through you -- only people in your extended trust network (direct trusted contacts also running Lantern, or their extended trusted contacts). That's why the second part is equally as important -- the more people you invite, the more likely you are to become an available access point for users in censored regions. **So please invite as many trusted contacts as you can!**

### <a name="hackers"/> Will Lantern make my computer vulnerable to hackers?
Lantern takes a number of precautions to make sure users are safe. First, Lantern does not allow any external computers to access your hard drive. Instead, Lantern simply acts as a conduit for your trusted contacts, relaying their requests to web pages on the open Internet as well as the replies from those web pages. External users have no access to your computer itself. Lantern also requires what's called mutual authentication for all connections, requiring that anyone connecting through you to the open Internet is someone you have a cryptographic key for, so someone who has learned about your computer through either being a trusted contact directly or through one of your trusted contacts. This ensures that not just anyone can connect to you through Lantern, but only people in your extended Lantern network.

### <a name="is-lantern-free"/> Is Lantern free? Will running it cost me anything?

Lantern is free as in money and as in freedom: free to use, modify, and
redistribute in accordance with its
[license](https://raw.github.com/getlantern/lantern/master/LICENSE). This
documentation is likewise distributed under a [[free license|LICENSE.txt]].

Running Lantern on your home or work network will not cost anything. If you connect primarily through a mobile data plan then Lantern can increase your bandwidth (as your trusted Lantern friends use your connection to get to the open internet). We recommend only using Lantern on unmetered Internet accounts.

### <a name="contributing"/> How can I contribute?

Please see the [[Contributing]] page.

### <a name="more"/> I have more questions, where do I go?

If you have more technical questions see the [Developers Q&A](https://github.com/getlantern/lantern/wiki/%5Bdevelopers%5D-Questions-and-Answers) page. If you still have more questions then ask on the [Lantern Forum](https://groups.google.com/forum/#!forum/lantern-users-en).