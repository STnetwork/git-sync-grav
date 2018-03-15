---
title: 'Install Composer.phar on CentOS 7'
process:
    markdown: true
    twig: true
twig_first: true
---

```
yum -y update
curl -sS https://getcomposer.org/installer | php
php composer.phar
```