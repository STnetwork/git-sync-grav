---
title: 'Layer 3 - Network Layer'
date: '01/11/2018 2:36pm'
twitterenable: true
twittercardoptions: summary
articleenabled: false
musiceventenabled: false
orgaenabled: false
orga:
    ratingValue: 2.5
orgaratingenabled: false
eventenabled: false
personenabled: false
restaurantenabled: false
restaurant:
    acceptsReservations: 'yes'
    priceRange: $
facebookenable: true
---

# <a href="/network/foundations-of-networking-networking-basics/3-osi-model" class="nav-button transform"><span></span></a>Layer 3 - Network Layer

![](layer-3-osi.png?cropResize=500,500)   {.center}

```
* Controls the operations of the subnetwork it is on.
* Determines best physical path for data.
* Uses network conditions to choose best path.
* Uses priority of service to determine best path.
* Uses other factors to determine best path.
```

**Network Layer** Provides Several Functions :
	* Routing
		* Routes frames among connected networks.
	* Subnet traffic control
		* Allows routers to send instructions to sending nodes to "throttle black" frame transmissions when buffers are filled.
	* Frame fragmentation
		* Determines frame size of routers located downstream.
		* Frame size called maximum transmission unit size.
		* Allows router to fragment frame into smaller sizes if needed.
		* Reassembles the full frame at destination.
	* Logical-physical address mapping
		* Translates logical addresses into physical addresses.
	* Subnet usage accounting
		* Has function that allows device to keep track of frames forwarded by subnet intermediate systems.
		* Uses this produce billing information.
		
**Network Layer** Communications Subnet :
	* Build headers used by Network Layer on other devices to route packets to destination.
	* Relieve higher layers of the need-to-know data transmission and switching technologies.
	* Use protocols on lower layers to send data to destinations separated by intermediate nodes.
	* Send information between adjacent nodes.
