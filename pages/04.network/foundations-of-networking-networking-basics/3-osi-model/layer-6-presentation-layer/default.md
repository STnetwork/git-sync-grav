---
title: 'Layer 6 - Presentation Layer'
date: '01/11/2018 1:35pm'
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

![](layer-6-osi.png?cropResize=500,500)   {.center}

```
* Formats data to be presented to the application layer.
* Translator for the network.
* At sending station translates data from application layer format to common format.
* At receiving station translates data from common format to format used by application layer.
```

**Presentation Layer Functions** :
	* Character code translation.
		* ASCII to EBCDIC
	* Data conversation.
		* Bit order
		* CR-CR/LF
		* Integer-floating point
	* Data compression
		* Reduces number of bits needed to transmit data.
	* Data encryption
		* Encryption of data for security purposes.
		* Encryption of passwords.
