---
title: Home
twig_first: true
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
musicalbumenabled: false
productenabled: false
product:
    ratingValue: 2.5
restaurantenabled: false
restaurant:
    acceptsReservations: 'yes'
    priceRange: $
facebookenable: true
---

<div>
<b-panel collapsible>
    <strong slot="header">Articles Linux</strong>
    <div class="content">
					<ul>
					{% for post in page.find('/linux/centos').children.order('date', 'desc').slice(0, 10) %}
							<li class="post-item">
							<strong>{{ post.date|date("d M Y") }} - <a href="{{ post.url }}">{{ post.title }}</a></strong>
							</li>
					{% endfor %}
					</ul>
    </div>
</b-panel>
</div>

---

<div>
<b-panel collapsible>
    <strong slot="header">Articles Windows</strong>
    <div class="content">
					<ul>
					{% for post in page.find('/windows/windows-server/windows-server-2016/dhcp').children.order('date', 'desc').slice(0, 10) %}
							<li class="post-item">
							<strong>{{ post.date|date("d M Y") }} - <a href="{{ post.url }}">{{ post.title }}</a></strong>
							</li>
					{% endfor %}
					</ul>
    </div>
</b-panel>
</div>

---

<div>
<b-panel collapsible>
    <strong slot="header">Articles Network</strong>
    <div class="content">
					<ul>
					{% for post in page.find('/network/foundations-of-networking-networking-basics/1-network-topologies').children.order('date', 'desc').slice(0, 10) %}
							<li class="post-item">
							<strong>{{ post.date|date("d M Y") }} - <a href="{{ post.url }}">{{ post.title }}</a></strong>
							</li>
					{% endfor %}
					{% for post in page.find('/network/foundations-of-networking-networking-basics/2-network-implementations').children.order('date', 'desc').slice(0, 10) %}
							<li class="post-item">
							<strong>{{ post.date|date("d M Y") }} - <a href="{{ post.url }}">{{ post.title }}</a></strong>
							</li>
					{% endfor %}
					{% for post in page.find('/network/foundations-of-networking-networking-basics/3-osi-model').children.order('date', 'desc').slice(0, 10) %}
							<li class="post-item">
							<strong>{{ post.date|date("d M Y") }} - <a href="{{ post.url }}">{{ post.title }}</a></strong>
							</li>
					{% endfor %}
					{% for post in page.find('/network/foundations-of-networking-networking-basics/4-tcp-ip-model').children.order('date', 'desc').slice(0, 10) %}
							<li class="post-item">
							<strong>{{ post.date|date("d M Y") }} - <a href="{{ post.url }}">{{ post.title }}</a></strong>
							</li>
					{% endfor %}
					{% for post in page.find('/network/foundations-of-networking-networking-basics/5-commonly-used-network-devices').children.order('date', 'desc').slice(0, 10) %}
							<li class="post-item">
							<strong>{{ post.date|date("d M Y") }} - <a href="{{ post.url }}">{{ post.title }}</a></strong>
							</li>
					{% endfor %}
					{% for post in page.find('/network/foundations-of-networking-ip-addressing/the-basics-of-numbering-systems-in-networking').children.order('date', 'desc').slice(0, 10) %}
							<li class="post-item">
							<strong>{{ post.date|date("d M Y") }} - <a href="{{ post.url }}">{{ post.title }}</a></strong>
							</li>
					{% endfor %}
					</ul>
    </div>
</b-panel>
</div>

<!--    --------------------------------------------------------------------------                           --> 
