---
title: 'Star & Hybrid Star Topologies'
date: '08/08/2017 2:38pm'
---

<div>
<nav class="breadcrumb is-medium" aria-label="breadcrumbs">
  <ul>
    <li><a href="/"><span class="icon is-small"><i class="fa fa-home"></i></span>Home<span></span></a></li>
    <li><a href="/network"><span class="icon is-small"><i class="fa fa-connectdevelop"></i></span><span>Network</span></a></li>
    <li><a href="/network/foundations-of-networking-networking-basics/1-network-topologies"></span>1. Network Topologies<span></span></a></li>
    <li><a href="#"></span>Star & Hybrid Star Topologies<span></span></a></li>
  </ul>
</nav>
</div>

---

[TOC]

---

## Hierarchical Star Topology  

![Alt text](hierarchical-star-topology.png?cropResize=500,500)   {.center}
```
* Most common Topology uses in LANs.
* More expensive than because needs more cables.
* Won't bring down Network with one damaged node.
* All nodes connected to a central Hub or Switch.
* Easy to Troubleshoot.
```
```
* Most common Topology uses in LANs.
* It's susceptible to a single point of failure.
* If whole Network goes down, Central Device is a problem.
* If only single node goes down, that node is the problem.
* This is only topology recognized in TIA/EIA 568-C Standard.
```
</br>

---
## Hybrid Star Topologies
```
* Combines normal Start Topology with some other Topology
* Physical Hybrid Start Topologies
* Physical-logical Hybrid Star Topologies
```
Physical Hybrid Star Topologies :
```
* Network containing two or more Physical Topologies
* Part of Network Ring another part Star
* Switches linked as Bus, but nodes connected as Star.
```

Physical-Logical Hybrid Star Topologies :
```
* Network physically looks one way but functions differently.
* Ring network that looks like a Star.
* Star network using Hub.
* Network looks like a Star but work like a Bus.
```

### Physical-Logical Hybrid Star Bus Topology
![Alt text](hybrid-star-bus-topology.png?cropResize=700,700)   {.center}

```
Network 1 & 2 are based on Star Topology but connect between each other using a Bus Topology
```


</br>

### Physical-Logical Hybrid Star Ring Topology
![Alt text](hybrid-star-ring-topology.png?cropResize=700,700)   {.center}

```
Network 1, 2 & 3 are based on Star Topology but connect between each other using a Ring Topology
```
