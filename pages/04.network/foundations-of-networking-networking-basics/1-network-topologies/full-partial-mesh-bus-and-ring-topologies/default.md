---
title: 'Full, Partial Mesh, Bus & Ring Topologies'
date: '08/08/2017 2:38pm'
---

<div>
<nav class="breadcrumb is-medium" aria-label="breadcrumbs">
  <ul>
    <li><a href="/"><span class="icon is-small"><i class="fa fa-home"></i></span>Home<span></span></a></li>
    <li><a href="/network"><span class="icon is-small"><i class="fa fa-connectdevelop"></i></span><span>Network</span></a></li>
    <li><a href="/network/foundations-of-networking-networking-basics/1-network-topologies"></span>1. Network Topologies<span></span></a></li>
    <li><a href="#"></span>Full, Partial Mesh, Bus & Ring Topologies<span></span></a></li>
  </ul>
</nav>
</div>

---

[TOC]

---

## Full Mesh Topology  

![Alt text](full-mesh-topology.png?cropResize=350,350)   {.center}
```
* All devices directly connected to all other devices.
* Provides Full Redundancy.
* Most expensive Type of Topology.
* Require multiple NICs and cables for each node, that's the reason why Full Mesh is the most expensive.
* Most likely to be found in WAN environments.
```
</br>
## Partial Mesh Topology

![Alt text](partial-mesh-topology.png?cropResize=350,350)   {.center}
```
* All devices directly connected to at least two other devices.
* Provides strong  Redundancy but not Full Redundancy.
* Not as expensive as Full Mesh.
* Require multiple NICs and cables for each machine.
* Most likely to be found in WAN environments.
* The Internet is a Partial Mesh.
```
---
</br>
## Bus Topology

![Alt text](bus-topology.png?cropResize=400,400)   {.center}
```
* It is one of the oldest Networking Topologies.
* All nodes connect directly to main cable called the Bus.
* It is simple to put together.
* Only one node can send a signal at a time.
* This is recommended for Network with 30 nodes or less.
* Contention is used to determine which node sends signal.
* The more nodes active, the more Collisions on Network.
* After Collision, all nodes again contend to send signal.
* To many collisions overload and bring down Network.
```


Some advantages & disadvantage to Bus Topology :
```
* Least expensive of the various Topologies.
* Single bad node or cable brings down whole network.
* Not part of current TIA/EIA 568-C Standard.
```
---
</br>
## Ring Topology

![Alt text](ring-topology.png?cropResize=400,400)   {.center}
```
* An older Network Topology.
* Similar to Bus Topology but connected in a Circle.
* Packet move in Ring around Network.
* Each node given opportunity to send a signal.
* No contention between nodes.
* Heavy traffic will not bring down Network.
* Heavy traffic will slow down Network.
* Single damaged node or cable can bring down Network.
* Not part of current TIA/EIA 568-C Standard for LAN Networks.
```
