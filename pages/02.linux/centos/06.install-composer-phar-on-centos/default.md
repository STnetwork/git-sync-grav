---
title: 'Install YARN on CentOS 7'
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
    <li><a href="#"></i></span><span>Install YARN on CentOS  7</span></a></li>
  </ul>
</nav>

---

## Introduction

**Fast**: Yarn caches every package it has downloaded, so it never needs to download the same package again. It also does almost everything concurrently to maximize resource utilization. This means even faster installs.

**Reliable**: Using a detailed but concise lockfile format and a deterministic algorithm for install operations, Yarn is able to guarantee that any installation that works on one system will work exactly the same on another system.

**Secure**: Yarn uses checksums to verify the integrity of every installed package before its code is executed.

## Features
* **Offline Mode**. If you've installed a package before, then you can install it again without an internet connection.
* **Deterministic**. The same dependencies will be installed in the same exact way on any machine, regardless of installation order.
* **Network Performance**. Yarn efficiently queues requests and avoids request waterfalls in order to maximize network utilization.
* **Network Resilience**. A single request that fails will not cause the entire installation to fail. Requests are automatically retried upon failure.
* **Flat Mode**. Yarn resolves mismatched versions of dependencies to a single version to avoid creating duplicates.
* **More emojis**. 🐈

## Installation

```
curl --silent --location https://dl.yarnpkg.com/rpm/yarn.repo | tee /etc/yum.repos.d/yarn.repo
curl --silent --location https://rpm.nodesource.com/setup_6.x | bash -
yum install yarn
```