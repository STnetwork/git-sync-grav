---
title: 'How Layer works Together'
date: '01/16/2018 10:33am'
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

# <a href="/network/foundations-of-networking-networking-basics/3-osi-model" class="nav-button transform"><span></span></a>How Layer works Together

![](howitworks.png?cropResize=1100,1100)   {.center}

In this first diagram, we see how we start out with data coming from the Operating System or more accurately, coming from applications running on the Operating System. And we see how each layer of the OSI model adds its own unique header. Now, each one of these headers that are added to each player of the OSI model, gives information to the computer on the other end about the data that is being transmitted.

* The application header for example, tells the computer on the other end what applications or services running on the operating system are being used for this data. 
* The presentation header contains information about encryption, compression, translation, anything like that that the computer on the other end needs to know in order to identify and use the data that's being transmitted. 
* The session layer presents information needed by the session layer on the receiving end to set up the session between the two processes that the data applies to.
* The transport layer contains information about the specific protocol or process needed by the session layer to set up the session with. 
* The network header provides information about the overall final destination of the data that's being transmitted. 
* The data link layer provides the address of the next node that the data needs to pass on to in order to reach its ultimate destination. It also includes a trailer that contains some error correction information.
* All this information is then converted into ones and zeros or encoded into ones and zeros and put on the media being used to transmit the data. That's what this particular graphic is showing us.