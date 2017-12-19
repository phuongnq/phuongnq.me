---
title: Install PHP 7.2 on MacOS with homebrew
date: 2017-12-18 20:21:26
tags: [php, macos, brew, tech, manual, english]
---

# Steps to update

[Homebrew](https://brew.sh/) is a package manager for MacOS. PHP 7.2 was officially [released](http://php.net/releases/7_2_0.php). I have just upgraded my local machine PHP version to 7.2 and this is the manual for doing it.

If you are not currently using *homebrew*, follow install manual in their [homepage](https://brew.sh/).

If you are currently using *homebrew*, make sure it is up to date:

```
brew update
brew upgrade
```

*upgrade* command may take time depends on how long you haven't used it!

If you'are not using *php7*, make sure to use `brew tap` to add repositories. `brew tap` is a command to add repositories other than officially added repository to *homebrew*. You could try enter command

```
brew tap
```

to check recently added repositories.

Now, add repositories for *php7*:

```
brew tap homebrew/dupes
brew tap homebrew/versions
brew tap homebrew/homebrew-php
```

If you have installed other version of *php* via *brew*, make sure to unlink it first. In my case, it was *php 7.1*.

```
brew unlink php71
```

Then install *php72*:

```
brew install php72
```

After everything is installed, check the result:

```
php --version
PHP 7.2.0 (cli) (built: Dec 16 2017 23:45:06) ( NTS )
Copyright (c) 1997-2017 The PHP Group
Zend Engine v3.2.0, Copyright (c) 1998-2017 Zend Technologies
```

# Note about PHP upgrade version

If you have to upgrade PHP version for your project, make sure to check their official upgrade manual. For example, [Migrating from PHP 7.1.x to PHP 7.2.x](http://php.net/manual/en/migration72.php). There are more upgrade manuals such as from version *5.6* to *7.0* or so on.

You can also use some open source tools to check if your source code is compatible with a certain *php* version. In my case, I used [PHPCompatibility](https://github.com/wimg/PHPCompatibility).