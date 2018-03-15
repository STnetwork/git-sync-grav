---
title: 'Grav CMS - CentOS 7 - NGINX'
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
    <li><a href="#"></i></span><span>Grav CMS - CentOS 7 - NGINX</span></a></li>
  </ul>
</nav>

---

[TOC]

----

## Introduction

Grav is a **Fast**, **Simple**, and **Flexible**, file-based Web-platform. There is **Zero** installation required. Just extract the ZIP archive, and you are already up and running. It follows similar principles to other flat-file CMS platforms, but has a different design philosophy than most. Grav comes with a powerful **Package Management System** to allow for simple installation and upgrading of plugins and themes, as well as simple updating of Grav itself.

The underlying architecture of Grav is designed to use well-established and best-in-class technologies to ensure that Grav is simple to use and easy to extend. Some of these key technologies include:

* [Twig Templating](http://twig.sensiolabs.org/): for powerful control of the user interface
* [Markdown](http://en.wikipedia.org/wiki/Markdown): for easy content creation
* [YAML](http://yaml.org/): for simple configuration
* [Parsedown](http://parsedown.org/): for fast Markdown and Markdown Extra support
* [Doctrine Cache](http://doctrine-orm.readthedocs.io/projects/doctrine-orm/en/latest/reference/caching.html): layer for performance
* [Pimple Dependency Injection Container](http://pimple.sensiolabs.org/): for extensibility and maintainability
* [Symfony Event Dispatcher](http://symfony.com/doc/current/components/event_dispatcher/introduction.html): for plugin event handling
* [Symfony Console](http://symfony.com/doc/current/components/console/introduction.html): for CLI interface
* [Gregwar Image Library](https://github.com/Gregwar/Image): for dynamic image manipulation

## Requirements

* CentOS 6 & 7
* VPS
* Nginx
* PHP 5.5.9 or higher. Check the [required modules list](https://learn.getgrav.org/basics/requirements#php-requirements)
* Composer (tutorial here)

## Install With Composer

```
composer create-project getgrav/grav /home/nginx/domains/stnetwork.fr/public/grav
```

```
Do not run Composer as root/super user! See https://getcomposer.org/root for details
Installing getgrav/grav (1.3.10)
  - Installing getgrav/grav (1.3.10): Downloading (100%)
Created project in /home/nginx/domains/stnetwork.fr/public/grav
Loading composer repositories with package information
Installing dependencies (including require-dev) from lock file
Package operations: 64 installs, 0 updates, 0 removals
  - Installing antoligy/dom-string-iterators (v1.0.0): Downloading (100%)
  - Installing composer/ca-bundle (1.0.8): Downloading (100%)
  - Installing doctrine/cache (v1.6.2): Downloading (100%)
  - Installing doctrine/collections (v1.3.0): Downloading (100%)
  - Installing donatj/phpuseragentparser (v0.7.0): Downloading (100%)
  - Installing erusev/parsedown (1.6.3): Downloading (100%)
  - Installing erusev/parsedown-extra (0.7.1): Downloading (100%)
  - Installing psr/log (1.0.2): Downloading (100%)
  - Installing filp/whoops (2.1.10): Downloading (100%)
  - Installing gregwar/cache (v1.0.12): Downloading (100%)
  - Installing gregwar/image (v2.0.21): Downloading (100%)
  - Installing seld/cli-prompt (1.0.3): Downloading (100%)
  - Installing league/climate (3.2.1): Downloading (100%)
  - Installing matthiasmullie/path-converter (1.1.0): Downloading (100%)
  - Installing matthiasmullie/minify (1.3.52): Downloading (100%)
  - Installing symfony/polyfill-mbstring (v1.5.0): Downloading (100%)
  - Installing symfony/var-dumper (v2.8.27): Downloading (100%)
  - Installing maximebf/debugbar (v1.14.0): Downloading (100%)
  - Installing miljar/php-exif (v0.6.3): Downloading (100%)
  - Installing monolog/monolog (1.23.0): Downloading (100%)
  - Installing psr/container (1.0.0): Downloading (100%)
  - Installing symfony/yaml (v2.8.27): Downloading (100%)
  - Installing symfony/event-dispatcher (v2.8.27): Downloading (100%)
  - Installing pimple/pimple (v3.2.2): Downloading (100%)
  - Installing rockettheme/toolbox (1.3.8): Downloading (100%)
  - Installing symfony/debug (v3.0.9): Downloading (100%)
  - Installing symfony/polyfill-iconv (v1.5.0): Downloading (100%)
  - Installing twig/twig (v1.35.0): Downloading (100%)
  - Installing symfony/finder (v3.3.9): Downloading (100%)
  - Installing symfony/dom-crawler (v3.3.9): Downloading (100%)
  - Installing symfony/css-selector (v3.3.9): Downloading (100%)
  - Installing symfony/console (v2.8.27): Downloading (100%)
  - Installing symfony/browser-kit (v3.3.9): Downloading (100%)
  - Installing stecman/symfony-console-completion (0.7.0): Downloading (100%)
  - Installing sebastian/diff (1.4.3): Downloading (100%)
  - Installing sebastian/recursion-context (1.0.5): Downloading (100%)
  - Installing sebastian/exporter (1.2.2): Downloading (100%)
  - Installing sebastian/comparator (1.2.4): Downloading (100%)
  - Installing phpunit/php-text-template (1.2.1): Downloading (100%)
  - Installing doctrine/instantiator (1.0.5): Downloading (100%)
  - Installing phpunit/phpunit-mock-objects (2.3.8): Downloading (100%)
  - Installing sebastian/version (1.0.6): Downloading (100%)
  - Installing sebastian/global-state (1.1.1): Downloading (100%)
  - Installing sebastian/environment (1.3.8): Downloading (100%)
  - Installing phpunit/php-timer (1.0.9): Downloading (100%)
  - Installing phpunit/php-file-iterator (1.4.2): Downloading (100%)
  - Installing phpunit/php-token-stream (1.4.11): Downloading (100%)
  - Installing phpunit/php-code-coverage (2.2.4): Downloading (100%)
  - Installing webmozart/assert (1.2.0): Downloading (100%)
  - Installing phpdocumentor/reflection-common (1.0.1): Downloading (100%)
  - Installing phpdocumentor/type-resolver (0.3.0): Downloading (100%)
  - Installing phpdocumentor/reflection-docblock (3.2.2): Downloading (100%)
  - Installing phpspec/prophecy (v1.7.2): Downloading (100%)
  - Installing phpunit/phpunit (4.8.36): Downloading (100%)
  - Installing psr/http-message (1.0.1): Downloading (100%)
  - Installing guzzlehttp/psr7 (1.4.2): Downloading (100%)
  - Installing guzzlehttp/promises (v1.3.1): Downloading (100%)
  - Installing guzzlehttp/guzzle (6.3.0): Downloading (100%)
  - Installing symfony/process (v3.3.9): Downloading (100%)
  - Installing facebook/webdriver (1.4.1): Downloading (100%)
  - Installing behat/gherkin (v4.4.5): Downloading (100%)
  - Installing codeception/codeception (2.3.5): Downloading (100%)
  - Installing fzaninotto/faker (v1.7.1): Downloading (100%)
  - Installing victorjonsson/markdowndocs (dev-master c9fa153): Cloning c9fa153b28
filp/whoops suggests installing whoops/soap (Formats errors as SOAP responses)
gregwar/image suggests installing behat/transliterator (Transliterator provides ability to set non-latin1 pretty names)
matthiasmullie/minify suggests installing psr/cache-implementation (Cache implementation to use with Minify::cache)
symfony/var-dumper suggests installing ext-symfony_debug ()
maximebf/debugbar suggests installing kriswallsmith/assetic (The best way to manage assets)
maximebf/debugbar suggests installing predis/predis (Redis storage)
miljar/php-exif suggests installing lib-exiftool (Use perl lib exiftool as adapter)
monolog/monolog suggests installing aws/aws-sdk-php (Allow sending log messages to AWS services like DynamoDB)
monolog/monolog suggests installing doctrine/couchdb (Allow sending log messages to a CouchDB server)
monolog/monolog suggests installing ext-amqp (Allow sending log messages to an AMQP server (1.0+ required))
monolog/monolog suggests installing ext-mongo (Allow sending log messages to a MongoDB server)
monolog/monolog suggests installing graylog2/gelf-php (Allow sending log messages to a GrayLog2 server)
monolog/monolog suggests installing mongodb/mongodb (Allow sending log messages to a MongoDB server via PHP Driver)
monolog/monolog suggests installing php-amqplib/php-amqplib (Allow sending log messages to an AMQP server using php-amqplib)
monolog/monolog suggests installing php-console/php-console (Allow sending log messages to Google Chrome)
monolog/monolog suggests installing rollbar/rollbar (Allow sending log messages to Rollbar)
monolog/monolog suggests installing ruflin/elastica (Allow sending log messages to an Elastic Search server)
monolog/monolog suggests installing sentry/sentry (Allow sending log messages to a Sentry server)
symfony/event-dispatcher suggests installing symfony/dependency-injection ()
symfony/event-dispatcher suggests installing symfony/http-kernel ()
sebastian/global-state suggests installing ext-uopz (*)
phpunit/php-code-coverage suggests installing ext-xdebug (>=2.2.1)
phpunit/phpunit suggests installing phpunit/php-invoker (~1.1)
codeception/codeception suggests installing codeception/specify (BDD-style code blocks)
codeception/codeception suggests installing codeception/verify (BDD-style assertions)
codeception/codeception suggests installing flow/jsonpath (For using JSONPath in REST module)
codeception/codeception suggests installing league/factory-muffin (For DataFactory module)
codeception/codeception suggests installing league/factory-muffin-faker (For Faker support in DataFactory module)
codeception/codeception suggests installing phpseclib/phpseclib (for SFTP option in FTP Module)
codeception/codeception suggests installing symfony/phpunit-bridge (For phpunit-bridge support)
Generating autoload files
> bin/grav install

Installing vendor dependencies
Do not run Composer as root/super user! See https://getcomposer.org/root for details
Loading composer repositories with package information
Installing dependencies from lock file
Package operations: 0 installs, 0 updates, 35 removals
  - Removing webmozart/assert (1.2.0)
  - Removing victorjonsson/markdowndocs (dev-master)
  - Removing symfony/process (v3.3.9)
  - Removing symfony/finder (v3.3.9)
  - Removing symfony/dom-crawler (v3.3.9)
  - Removing symfony/css-selector (v3.3.9)
  - Removing symfony/browser-kit (v3.3.9)
  - Removing stecman/symfony-console-completion (0.7.0)
  - Removing sebastian/version (1.0.6)
  - Removing sebastian/recursion-context (1.0.5)
  - Removing sebastian/global-state (1.1.1)
  - Removing sebastian/exporter (1.2.2)
  - Removing sebastian/environment (1.3.8)
  - Removing sebastian/diff (1.4.3)
  - Removing sebastian/comparator (1.2.4)
  - Removing psr/http-message (1.0.1)
  - Removing phpunit/phpunit-mock-objects (2.3.8)
  - Removing phpunit/phpunit (4.8.36)
  - Removing phpunit/php-token-stream (1.4.11)
  - Removing phpunit/php-timer (1.0.9)
  - Removing phpunit/php-text-template (1.2.1)
  - Removing phpunit/php-file-iterator (1.4.2)
  - Removing phpunit/php-code-coverage (2.2.4)
  - Removing phpspec/prophecy (v1.7.2)
  - Removing phpdocumentor/type-resolver (0.3.0)
  - Removing phpdocumentor/reflection-docblock (3.2.2)
  - Removing phpdocumentor/reflection-common (1.0.1)
  - Removing guzzlehttp/psr7 (1.4.2)
  - Removing guzzlehttp/promises (v1.3.1)
  - Removing guzzlehttp/guzzle (6.3.0)
  - Removing fzaninotto/faker (v1.7.1)
  - Removing facebook/webdriver (1.4.1)
  - Removing doctrine/instantiator (1.0.5)
  - Removing codeception/codeception (2.3.5)
  - Removing behat/gherkin (v4.4.5)
Generating optimized autoload files


Cloning Bits
============

SUCCESS cloned https://github.com/getgrav/grav-plugin-problems -> /home/nginx/domains/stnetwork.fr/public/grav/user/plugins/problems

SUCCESS cloned https://github.com/getgrav/grav-plugin-error -> /home/nginx/domains/stnetwork.fr/public/grav/user/plugins/error

SUCCESS cloned https://github.com/getgrav/grav-plugin-markdown-notices -> /home/nginx/domains/stnetwork.fr/public/grav/user/plugins/markdown-notices

SUCCESS cloned https://github.com/getgrav/grav-theme-antimatter -> /home/nginx/domains/stnetwork.fr/public/grav/user/themes/antimatter
```

cd  /home/nginx/domains/stnetwork.fr/public/grav


Install Plugin
bin/gpm install admin highlight git-sync sync haywire -y
bin/gpm install highlight
bin/gpm install git-sync sync

