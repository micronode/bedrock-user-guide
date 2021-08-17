# The benefits of a Proxy
This pages addresses some uses of a proxy component to control ingress and egress traffic for your system.

## Overview

A proxy is essentially a network-level component that sits between your service and external integration points. This could be for traffic initiated externally (ingress) or traffic flowing out from your system (egress).

## Proxy vs Firewall

At first glance it may seem that a proxy performs a similar function as a firewall, however they are fundamentally different. Firewalls are aimed at blocking or allowing network connectivity on specific ports, regardless of the data that flows on said ports or where it is coming from or going to.

A proxy, on the other hand, is concerned with the source/destination of data, and may even inspect network packets as they are received to determine the validity of requests. As this can be a CPU intensive activity it is important to use proxying features judicously so as to not impact on system performance.
