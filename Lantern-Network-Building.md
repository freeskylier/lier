Lantern depends on a strong trust network of users that spans the censorship divide and that includes enough Give mode users to have proxies available when censored users need them.

To this end, both Give and Get mode users need tools to help them grow their trust networks.  The benefits of growing the Lantern trust network aren't immediately palpable to users.  It may take Give mode users a while before they see any Get mode users connecting through their proxy. Due to the immediate availability of fallback proxies, Get mode users may not sense the importance of building their trust network in order to improve the speed and reliability of the Lantern proxy network.

Given these challenges, Lantern should both make it as easy as possible to grow one's trust network, as well as provide education and encouragement to get users to engage in this process.

The tools for growing ones network are universally applicable, while education and encouragement need to be sensitive to differences in the Give and the Get mode experiences.

This document outlines approaches for addressing all of these aspects of building the trust network.

note - It is important to remember that much network building can proceed informally and outside of the Lantern application - ultimately Lantern just needs to know once the connection has been made.  Before going too far down the road of building specific tooling, we should make sure to talk with our "connnectors", i.e. the people who have relationships that bridge the censorship divide and who are likely to be the lynchpins of the Lantern trust network in its early stages.

### Tools

#### Finding and inviting friends

Lantern should make it easy to find Lantern friends, in particular ones who can help bridge the censorship divide.  To this end, Lantern should integrate with popular social networks

 * Email via Google contacts (already implemented)
 * Google+ circles
 * LinkedIn
 * Facebook
 * Twitter

Not all friends are created equally.  We want to connect users from uncensored countries with users in censored countries.  To this end, we want to prioritize relationships where:

 1. The friends have different censorship status (e.g. U.S. and China)
 2. One of the friends has connections to people with a different censorship status

Item 1 can be accomplished with most social APIs that include location information about friends (which is most of them).  The problem is that there aren't necessarily a lot of people who have friends across the censorship divide.

Item 2 can be accomplished with LinkedIn.  The upside to this is that it can help us expand the pool of "connectors".

What else do we need here?  Many social networking invite systems have a way of tracking replies, resending reminders and so on...

### Education and Encouragement

There are many angles to this.  It is instructive to look at what both social networks and electronic appliances like the [Nest thermostat](http://nest.com/).

Social networks constantly prod you to build out your network by:

 * Suggesting new friends based on existing friends and interests
 * Suggesting new friends based on contacts in your contact list
 * Providing a mechanism for friends to message each other
 * Reminding you about events in friends' lives (e.g. birthdays) to get you to reach out and communicate with that friend.  In the case of Lantern, this could be something like "Joe proxied a request for Sally for the first time ever" (see https://github.com/getlantern/lantern/issues/1048)

The Nest thermostat has some interesting parallels with Lantern because it's also something with which you interact infrequently and that you use to meet a very specific goal (saving energy while staying comfortable).  Two things that the Nest thermostat does particularly well are:

 1. It collects a variety of interesting metrics but distills these down into a single easy-to-understand number, namely how many hours your heating/cooling system ran in the last month.  From there, one can drill down into the other metrics to understand what led to that usage, but having that single bottom-line number makes it easy to keep track of what's happening without having to invest too much mental bandwidth.

 2. It uses monthly emails to let you know how you're doing, make you feel like part of a community and remind you that there's a team of people constantly making Nest better.

In the case of Lantern, Give and Get mode users have complimentary but slightly different goals.

Get mode users are interested in availability and speed.  Give mode users are interested in helping out as many people as possible but also limiting how much of their bandwidth is consumed.

This suggests a hierarchy of metrics like the following (all broken down on a monthly basis if possible):

 * Number of bytes proxied
   * Number of peers active at any time during month
   * Number of hours that Lantern was running (see https://github.com/getlantern/lantern/issues/1025)
   * Top 5 domains proxied by # of requests (see https://github.com/getlantern/lantern/issues/1027)
   * ???

The first two sub-metrics, # of peers and # of hours, present points for clear calls to action when the numbers are low, namely "grow your network" and "run lantern".

These are both things about which we can and should remind people via email.

#### Email Schedule

 1. Welcome to Lantern
 2. (If user hasn't added any friends) - Add Some Friends
 3. Monthly Status Update
 4. ???


### Related Tickets

 * https://github.com/getlantern/lantern/issues/988
 * https://github.com/getlantern/lantern/issues/972
 * https://github.com/getlantern/lantern/issues/971
 * https://github.com/getlantern/lantern/issues/969
 * https://github.com/getlantern/lantern/issues/967
 * https://github.com/getlantern/lantern/issues/966
 * https://github.com/getlantern/lantern/issues/965
 * https://github.com/getlantern/lantern/issues/654
 * https://github.com/getlantern/lantern/issues/964
 * https://github.com/getlantern/lantern/issues/647
 * https://github.com/getlantern/lantern/issues/580
 * https://github.com/getlantern/lantern/issues/960
 * https://github.com/getlantern/lantern/issues/947
 * https://github.com/getlantern/lantern/issues/946
 * https://github.com/getlantern/lantern/issues/945
 * https://github.com/getlantern/lantern/issues/937