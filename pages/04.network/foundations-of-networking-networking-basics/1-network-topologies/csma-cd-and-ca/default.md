---
title: 'CSMA/CD & CA'
date: '08/08/2017 2:38pm'

---

<div>
<nav class="breadcrumb is-medium" aria-label="breadcrumbs">
  <ul>
    <li><a href="/"><span class="icon is-small"><i class="fa fa-home"></i></span>Home<span></span></a></li>
    <li><a href="/network"><span class="icon is-small"><i class="fa fa-connectdevelop"></i></span><span>Network</span></a></li>
    <li><a href="/network/foundations-of-networking-networking-basics/1-network-topologies"></span>1. Network Topologies<span></span></a></li>
    <li><a href="#"></span>CSMA/CD & CA<span></span></a></li>
  </ul>
</nav>
</div>
---

# Contention-Based Network Access

* Computers competing for Network Access
* Two types of Contention-Based Access :
	* Carrier Sensing Media Access/Collision Detection.
		* CSMA/CD
		* Method most commonly used by wired Ethernet
	* Carrier Sensing Media Access/Collision Avoidance
		* CSMA/CA
		* Method most commonly used by Wi-Fi

---

## CSMA/CD  
</br>
![Alt text](csma.png?cropResize=600,600)   {.center}

```
* Node listens for Traffic on Network.
* If traffic not heard, node releases Packet onto Network.
* If two Nodes release Packet at the same time, the Packets hit each other and a Collision occurs.
* A Collision causes a Power Spike heard by all Nodes.
* A Collision destroys the Data contained in the two Packets.
```
</br>
![Alt text](csma2.png?cropResize=600,600)   {.center}

```
* If no Collision, then Transmission was successful.
* Network is now freed up for another node to transmit.
```
</br>
![Alt text](csma4.png?cropResize=600,600)   {.center}

```
* If a Collision occurs, all Nodes start internal Clock set to a random number of milliseconds.
* When times runs down, each node can attempt to send new transmission.
```
---

## CSMA/CA
</br>
![Alt text](csma-ca3.png?cropResize=600,600)   {.center}

```
* Works similarly to CSMA/CD.
* Release warning Packet before releasing Data Packet.
* If other Nodes hear warning Packet, they won't transmit.
* Once Data Packet heard, other Nodes are able to transmit.
* Two warning Packets transmitted at same time cause a Collision.
```
