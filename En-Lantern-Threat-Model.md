# Lantern Threat Model

## Abstract

We discuss the threat model for Lantern as a whole, addressing Lantern
subsystems in more detail where appropriate. We discusse the problems Lantern
solves as well as what it explicitly does not solve.

## Capabilities of Adversaries

Lantern assumes that all adversaries are equipped with sophisticated Deep
Packet Inspection (DPI) technology capable of inspecting, modifying, or
blocking every packet going in and out of the region they control (typically
country borders) as well as within that region. Adversaries are capable of
applying sophisticated system-wide rules to standard protocols. We assume these
DPI tools are capable of identifying all standardized protocols and can be
taught to identify custom protocols.

## Limitations of Adversaries

Adversaries are assumed to have limited ability to manipulate traffic on
individual connections.

## Goals of Lantern

Lantern's primary goal is to provide a blocking-resistant way to provide access
to all web sites on the internet, particularly sites that are blocked in
certain countries or regions. It explicitly **does not to hide your IP address
from those sites**. If users are performing some task that might put them in
danger, we encourage the use of tools that devote more resources to protecting
users' anonymity online, such as [[Tor|http://www.torproject.org]].
