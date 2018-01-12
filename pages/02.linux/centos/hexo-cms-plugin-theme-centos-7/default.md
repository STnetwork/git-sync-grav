---
title: 'Hexo CMS  - Plugin - Theme - CentOS 7'
process:
    markdown: true
    twig: true
twig_first: true
---

# <a href="/linux/centos" class="nav-button transform"><span></span></a>Hexo CMS on CentOS 7 - Plugin - Theme

---

<nav class="breadcrumb is-medium" aria-label="breadcrumbs">
  <ul>
    <li><a href="/"><span class="icon is-small"><i class="fa fa-home"></i></span>Home<span></span></a></li>
    <li><a href="/linux"><span class="icon is-small"><i class="fa fa-linux"></i></span><span>Linux</span></a></li>
    <li><a href="/linux/centos"></i></span><span>CentOS</span></a></li>
    <li><a href="#"></i></span><span>Hexo CMS on CentOS 7 - Plugin - Theme</span></a></li>
  </ul>
</nav>

---

* [Introduction](/linux/centos/hexo-cms-plugin-theme-centos-7#introduction)
	* [Prerequisites](/linux/centos/hexo-cms-plugin-theme-centos-7#prerequisites)
* [Install Dependencies](/linux/centos/hexo-cms-plugin-theme-centos-7#install-dependencies)
* [Install Hexo](/linux/centos/hexo-cms-plugin-theme-centos-7#install-hexo)
* [Initialize your Project](/linux/centos/hexo-cms-plugin-theme-centos-7#initialize-your-project)
	* [Launch Server](/linux/centos/hexo-cms-plugin-theme-centos-7#launch-server)
* [Apply Theme](/linux/centos/hexo-cms-plugin-theme-centos-7#apply-theme)
	* [Edit the main `_config.yml` for apply the new theme](/linux/centos/hexo-cms-plugin-theme-centos-7#edit-the-main-_configyml-for-apply-the-new-theme)
	* [Configure the theme in another `_config.yml`](/linux/centos/hexo-cms-plugin-theme-centos-7#configure-the-theme-in-another-_configyml)
* [Apply a Plugin](/linux/centos/hexo-cms-plugin-theme-centos-7#apply-a-plugin)
    * [Plugin Admin Interface](/linux/centos/hexo-cms-plugin-theme-centos-7#plugin-admin-interface)
    * [Password protection of the Interface Admin](/linux/centos/hexo-cms-plugin-theme-centos-7#password-protection-of-the-interface-admin)
* [Clean & Generate Static](/linux/centos/hexo-cms-plugin-theme-centos-7#clean-generate-static)

----

## Introduction

You will be able to install your own Blog with [Hexo](https://hexo.io/) on CentOS 7 or other Distribution Linux by following this article.
Hexo is an awsome tool to create a Simple, Fast & Powerful blog framework, it generates static files with a beautiful theme in seconds.
We can write posts in [Markdows](http://daringfireball.net/projects/markdown/) or other languages.

### Prerequisites
* VPS or Local Machine Linux, in my case it's on CentOS 7
* System Up To Date
* NVM (optional), NPM & Node.JS
* LEMP (optional) in my case it's [CENTMIN MOD](http://centminmod.com/)
* Git

----

## Install Dependencies

Before to start the installation of Hexo, we have to launch some `npm install` for the dependencies :

``` bash
npm install cnpm -g --registry=https://registry.npm.taobao.org
npm install -g minimatch@latest
npm install marked --save
```

----

## Install Hexo

Install the Hexo command line interface (CLI) with the Node Package Manager `npm` anywhere you want :

``` bash
npm install hexo-cli -g
```

----

## Initialize your Project

Go into your folder where you want install your blog, in my case that's `(/home/nginx/domains/stnetwork.fr/public/)` :

``` bash
cd /home/nginx/domains/stnetwork.fr/public/
```

Run the following commands to initialise Hexo in the target folder & apply the good permissions :

``` bash
hexo init STnetwork
cd STnetwork
npm install
chown -R $USER:$USER /home/nginx/domains/stnetwork.fr/public/STnetwork/
chmod -R 755 /home/nginx/domains/stnetwork.fr/public/STnetwork/
```

### Launch Server

Verify the server can run correctly :

``` bash
hexo server
```

Enter `localhost:4000` in your Browser, you should see the Hexo blog.
We will see in the Part IV how to configure the server with Nginx.

----

## Apply Theme

You can choose a theme from [this link](https://hexo.io/themes/), I have choose [cactus-dark](https://github.com/probberechts/cactus-dark).
Go into folder project, for your information, we have to run all commands concerning hexo in the root of project in my case my root folder is `(/home/nginx/domains/stnetwork.fr/public/STnetwork/)`  :

``` bash
cd /home/nginx/domains/stnetwork.fr/public/STnetwork/
git clone https://github.com/probberechts/cactus-dark.git themes/cactus-dark
```


### Edit the main `_config.yml` for apply the new theme

Open `_config.yml` who is in `(/home/nginx/domains/stnetwork.fr/public/STnetwork/)` with your favorite text editor and change the teme as below :.

``` bash
# This is a comment in .yml files
# theme: landscape
theme: cactus-dark
```


### Configure the theme in another `_config.yml`

We can configure the theme cactus-dark with an antoher `_config.yml` who is in `(/home/nginx/domains/stnetwork.fr/public/STnetwork/themes/cactus-dark)`.

More information about [the configuration of this theme cactus-dark](https://github.com/probberechts/cactus-dark#configuration).

----

## Apply a Plugin

As usual we go into the folder project and install the plugin we want, in this case this is a plugin for admin interface Hexo, with this plugin we can create Posts, Pages and apply some Configurations from an interface [Here the list of all plugins Hexo available](https://hexo.io/plugins/).


### Plugin Admin Interface

``` bash
cd /data/wwwroot/stnetwork.fr/STnetwork/
npm install --save hexo-admin
npm install hexo-pagination --save
```

Then we can access in this interface from `localhost:4000/admin/`

![Alt text](https://raw.githubusercontent.com/jaredly/hexo-admin/master/docs/pasted-1.png)



### Password protection of the Interface Admin

For apply a password protection for access to the Interface Admin you must add these lines as below in your main `_config.yml` :

``` bash
admin:
  username: myfavoritename
  password_hash: be121740bf988b2225a313fa1f107ca1
  secret: a secret something
```

The `password_hash` is the bcrypt hash of your password. The `secret` is used to make the cookies secure, so it's a good idea to have it be long and complicated.

A utility in Hexo admin's Settings can hash your password and generate the `admin` section for you. Start Hexo and go to `Settings > Setup authentification` and fill out your information. Copy the generated YAML into your main `_config.yml`.

----

## Clean & Generate Static

We can generate static files with the commands as below, this part is especially for Nginx that we will see in the next Part IV.

``` bash
hexo clean
hexo generate
```
