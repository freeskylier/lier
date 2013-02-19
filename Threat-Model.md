# Threat Model

(work in progress)


## Abstract

We discuss the threat model for Lantern as a whole, addressing Lantern
subsystems in more detail where appropriate. We discuss the problems Lantern
solves as well as what it explicitly does not solve.


## Capabilities of Adversaries

Lantern assumes that all adversaries are equipped with sophisticated Deep
Packet Inspection (DPI) technology capable of inspecting, modifying, or
blocking every packet going in and out of the region they control (typically
country borders) as well as within that region. Adversaries are capable of
applying sophisticated system-wide rules to standard protocols. We assume these
DPI tools are capable of identifying all standardized protocols and can be
taught to identify custom protocols. Using these tools, adversaries can:

* Block IP addresses of their choosing
* Block specific DNS lookups
* Use any unique characteristics of given network connections to block and drop that connection, such as TLS handshakes

In addition, adversaries are assumed to be able to:

* Control their own certificate authorities to issue certificates for any domain
* Pose as legitimate users on the network in an attempt to learn of as many access points as possible



## Limitations of Adversaries

Adversaries are assumed to have limited ability to manipulate traffic on
individual connections.


## Goals of Lantern

Lantern's primary goal is to provide a blocking-resistant way of offering
access to all web sites on the internet, particularly sites that are blocked in
certain regions. It **does not necessarily hide your IP address from those
sites**. If you are performing some task that might put you in danger, we
encourage the use of tools that devote more resources to protecting your
anonymity online, such as [Tor](http://www.torproject.org).
