Currently, Lantern maintains a set of [cloud fallback proxy servers](https://github.com/getlantern/lantern/wiki/Lantern-Cloud-Servers) for users who aren't able to connect through a peer in their trust network, either because no such peers are online or no such peers are reachable.

In addition to helping users use Lantern to access the internet, these fallback proxies are vitally important during the installation and setup of Lantern, as they allow users to access Google Talk to get onto the Lantern network in countries where Google Talk is blocked.

At the moment, every Lantern instance is assigned to one, and only one, fallback proxy by the following algorithm:

* If the Lantern user is a root user (invited by Lantern, not another Lanter user?), spool up a new fallback proxy for this user

* If the Lantern user was invited by another Lantern user that already has a fallback proxy, assign the new user to the existing fallback proxy

In this way, we end up with a sub-tree of our trust graph consisting of users who all share the same fallback proxy.  This is important from an availability perspective because it minimizes the breadth of the impact if this sub-tree should become compromised by censors.

This creates two problems:

1. Some proxies end up over-utilized because the sub-tree contains too many users.  This adversely impacts the user experience of users who rely on those fallback proxies.

2. Some proxies end up under-utilized because the sub-tree contains too few users.  This ends up wasting capacity that costs money to maintain.

In order to address both of these problems, we need to introduce some sort of load balancing that allows us to:

1. Use multiple fallback proxies to serve a single sub-tree of the trust graph.

2. Allow a single fallback proxy to serve multiple sub-trees of the trust graph.

## Solution for Problem 1 - Multiple Fallback Proxies per Sub-Tree

Because this problem impacts the user experience, it needs to be addressed first.

Currently, fallback proxies are assigned to users during the invitation process.  This is necessary because it allows us to provide customized installers that contain the correct fallback proxy and allow Lantern users to get online via that fallback proxy in case Google Talk is blocked in their country.

Unfortunately, the invitation process does not give us a good mechanism to load balance amongst fallback proxies because we don't know how heavily utilized a fallback proxy is until someone actually installs Lantern and starts using it.  In the most extreme case, one can imagine that a very lightly utilized fallback ends up getting included in a large number of invitations.  If all, or many, of these invitations get accepted and these users end up actively using Lantern, their fallback proxy will end up over-utilized.

This means that we need a mechanism for re-balancing after invitations have already gone out.  In the long-term, an approach that might work well is to treat fallback proxies like any peer proxy and rely in the XMPP/Kaleidoscope mechanism to advertise the availability of these.  This would allow us to add and remove them as necessary and clients would automatically load balance between them.  This requires some serious thought, so we need an alternative in the short term.

Here's a proposal for how to do it in the short term:

1. Currently, LanternUser keeps track of an installerLocation corresponding to a custom installer that encapsulates the fallback proxy for that user.  Let's change this to be a List of installerLocations that can keep track of new installers as we add them.

2. When sending out an invitation from an existing user with an existing fallback proxy, use the most recent installerLocation from the list (as opposed to just the single installerLocation like we do today)

3. Have fallback proxies track and report the maximum # of distinct clients that have connected to that proxy via Librato (already implemented)

4. Implement a batch job in the controller that monitors all fallback proxies for activity using the metric from #3.  If a fallback proxy gets too busy (i.e. # of distinct clients exceeds threshold):

   1. Spin up a new fallback proxy for the root LanternUser of the sub-tree

   2. Randomly reassign N LanternUsers in the sub-tree to the new fallback proxy, where N = max distinct clients - threshold

5. Implement a protocol between Lantern instances and the controller (probably on the XMPP channel) that tells Lantern instances which fallback proxy they should be using.

6. In the Lantern client, if the client is told to use a different fallback proxy than the one currently in use, switch to the new fallback proxy and save this in .lantern for future startups



