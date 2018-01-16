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

![](howitworks.png?lightbox=1400,1100&resize=800,800)   {.center}

In this first diagram, we see how we start out with data coming from the Operating System or more accurately, coming from applications running on the Operating System. And we see how each layer of the OSI model adds its own unique header. Now, each one of these headers that are added to each player of the OSI model, gives information to the computer on the other end about the data that is being transmitted.

* The application header for example, tells the computer on the other end what applications or services running on the operating system are being used for this data. 
* The presentation header contains information about encryption, compression, translation, anything like that that the computer on the other end needs to know in order to identify and use the data that's being transmitted. 
* The session layer presents information needed by the session layer on the receiving end to set up the session between the two processes that the data applies to.
* The transport layer contains information about the specific protocol or process needed by the session layer to set up the session with. 
* The network header provides information about the overall final destination of the data that's being transmitted. 
* The data link layer provides the address of the next node that the data needs to pass on to in order to reach its ultimate destination. It also includes a trailer that contains some error correction information.
* All this information is then converted into ones and zeros or encoded into ones and zeros and put on the media being used to transmit the data. That's what this particular graphic is showing us.

---

![](howitworks2.png?lightbox=1400,1100&resize=800,800)   {.center}

Now the way the computer handles this or the way the datagrams are handled by the computer is shown in this diagram. Basically, you start out with the basic data and as each layer of the OSI model adds its own header or trailer in the case of data link layer, then whatever was in the datagram before the new header was added becomes data contained in the overall datagram.

The result is that as the data moves through or down the OSI model, it becomes larger and larger and larger. This is illustrated by the fact that data starts out as yellow and as it moves down the OSI layers the yellow portion becomes larger and larger and larger because it is containing the headers of the layer above it. This data section becoming larger and larger and larger is what is called overhead and so the more information contained in each one of the headers of the OSI model, the larger the overall data portion of the datagram becomes.

So one of the goals of networking is to keep the headers as small as possible so that we can minimize the amount of data or the overhead that the network has to handle in order to process each one of the datagrams that are transmitted.

---

![](howitworks3.png?lightbox=2000,1100&resize=800,800)   {.center}