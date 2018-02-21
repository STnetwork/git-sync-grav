---
title: 'Hexadecimal Numbering System'
twittercardoptions: summary
articleenabled: false
musiceventenabled: false
orgaenabled: false
orga:
    ratingValue: 2.5
orgaratingenabled: false
eventenabled: false
personenabled: false
musicalbumenabled: false
productenabled: false
product:
    ratingValue: 2.5
restaurantenabled: false
restaurant:
    acceptsReservations: 'yes'
    priceRange: $
---

#  <a href="https://stnetwork.fr/network/foundations-of-networking-ip-addressing/the-basics-of-numbering-systems-in-networking" class="nav-button transform"><span></span></a>Hexadecimal Numbering System



---

<div>
<nav class="breadcrumb is-medium" aria-label="breadcrumbs">
  <ul>
    <li><a href="/"><span class="icon is-small"><i class="fa fa-home"></i></span>Home<span></span></a></li>
    <li><a href="/network"><span class="icon is-small"><i class="fa fa-connectdevelop"></i></span><span>Network</span></a></li>
    <li><a href="/network/foundations-of-networking-ip-addressing"></span>Foundations of Networking - IP Addressing<span></span></a></li>
    <li><a href="/network/foundations-of-networking-ip-addressing/the-basics-of-numbering-systems-in-networking"></span>1. The Basics of Numbering Systems in Networking<span></span></a></li>
    <li><a href="#"></span>Hexadecimal Numbering System<span></span></a></li>
  </ul>
</nav>
</div>

---

## Hexadecimal Numbering System

```
• Is a base 16 numbering system
• Working with Hexadecimal easier than Binary
• No need to convert to Decimal or Vice Versa
• Only convert between Binary and Hexadecimal
• Hexadecimal is used to shorten binary numbers
• It is easier to read
• It is easier to differentiate between Hexadecimal values than binary values
• Every 4 Binary bits result in 1 in Hexadecimal value
• The symbols used to represent Hexadecimal values are 0-9 and A-F
```

---

## Converting Binary to Hexadecimal

```

• 1101 0010 1001 0010 0111 1010 1110 0001
•  D    2    9    2    7    A    E    1
```

---

## Converting Binary to Decimal

| 2^7 | 2^6 | 2^5 | 2^4 | 2^3 | 2^2 | 2^1 | 2^0 |
| ----- |-----| ----- | ----- | ---- | ----- | ----- | ----- |
| 128 | 64  | 32  | 16  | 8   | 4   | 2   | 1   |
| 1   | 0   | 1   | 1   | 0   | 0   | 0   | 1   |

```
• All we have to is, Add up all the boxes with a 1 in them.
• 128 + 32 + 16 + 1 = 177
```

---

## Converting Decimal to Binary 

| 2^7 | 2^6 | 2^5 | 2^4 | 2^3 | 2^2 | 2^1 | 2^0 |
| ----- |-----| ----- | ----- | ---- | ----- | ----- | ----- |
| 128 | 64  | 32  | 16  | 8   | 4   | 2   | 1   |
| 1   | 1   | 0   | 0   | 1   | 0   | 1   | 1   |

```
• 203
• 203 - 128 = 75
• **Place** 1 in 128 box

• 75
• 75 - 64 = 11 
• **Place** 1 in 64 box

• 11
• 11 - 8 = 3
• **Place** 1 in 8 box

• 3
• 3 - 2 = 1 
• **Place** 1 in 2 box

• 1
• 1 - 1 = 0 
• **Place** 1 in 1 box
```