---
title: 'Encapsulation & de-Encapsulation'
date: '01/11/2018 1:33pm'
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

# <a href="/network/foundations-of-networking-networking-basics/3-osi-model" class="nav-button transform"><span></span></a>Encapsulation & de-Encapsulation

![](Encapsulation-&-de-Encapsulation.png?cropResize=600,600)   {.center}

```
* Each layer of OSI model adds a header to the data.
* Layer also create a unit used to send or receive data.
* The process of moving data down the OSI model is called encapsulation.
* The process of moving data up the OSI model is called de-encapsulation.
```

**Each Layer Has an Encapsulation Unit** :

* Information on application layer through session layer is called data.
* Transport Layer converts data to segments.
* Network Layer converts segments to packets.
* Data Link Layer converts Packets to Frames.
* Physical Layer converts frames to bits.