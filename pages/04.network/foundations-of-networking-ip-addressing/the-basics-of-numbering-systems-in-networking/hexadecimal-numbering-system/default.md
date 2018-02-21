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
    <li><a href="#"></span>Binary Numbering System<span></span></a></li>
  </ul>
</nav>
</div>

---

## Base 10 Numbering System

```
Base 10 Numbering System :
• The numbering system people use it the Base 10 numbering system, also called Decimal system.
• We use 10 symbols to represent values from 0 to 9.
• Each value in the position to the left is multiplied by 10 times the value located in the position to the right.
• We have 1000s, 100s, 10s, 1s, and so on.
• 4 * 1000 + 7 * 100 + 8 * 10 + 3 * 1 = 4783
```

---

## Binary 2 Numbering System

```
Base 2 Numbering System also called Binary :
• It only use 2 symbols : 0 and 1
• Each value symbol to the left is multiplied by 2 times the value of the symbol to the right.
• As result, we have 16s, 8s, 4s, 2s, and 1s.
• 1 * 16 + 0 * 8 + 1 * 4 + 1 * 2 + 1 * 1 = 10111, The decimal equivalent is 23
• All numbers in Binary are represented by 1s and 0s.
• In electronics, 1 is represented by power being On or at a Higher Voltage.
• 0 is represented by power being Off or at Lower Voltage.
• In networking, we usually only need to convert numbers with 8 bits or less.
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