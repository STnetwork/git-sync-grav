---
title: 'NVM NPM NodeJS - CentOS 7'
process:
    markdown: true
    twig: true
twig_first: true
---

<nav class="breadcrumb is-medium" aria-label="breadcrumbs">
  <ul>
    <li><a href="/"><span class="icon is-small"><i class="fa fa-home"></i></span>Home<span></span></a></li>
    <li><a href="/linux"><span class="icon is-small"><i class="fa fa-linux"></i></span><span>Linux</span></a></li>
    <li><a href="/linux/centos"></i></span><span>CentOS</span></a></li>
    <li><a href="#"></i></span><span>NVM - NPM - NodeJS - CentOS 7</span></a></li>
  </ul>
</nav>

----

## NVM

NVM - Node Version Manager is a Simple bash script to manage multiple active node.js versions. It allows us to easily install and switch between versions.


``` bash
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.8/install.sh | bash
nvm --version
0.33.8
nvm install node
npm -v
5.6.0
```
