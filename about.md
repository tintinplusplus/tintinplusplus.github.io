---
layout: page
title: About
permalink: /
---


The TinTin++ Unofficial's User Group is an attempt to bring the TinTin++ community together and improve the way that we share code and documentation. This user's group is brand new and is currently being maintained by @nfarrar.

I've invited all the user's I know about on github to the organization as contributors so you should have access to contribute and fix content, should you so desire. :) If you didn't get an invite and want to contribute, shoot a message or email to @nfarrar.


Documentation
-------------
The [Unofficial TinTin++ Documentation](https://tintinplusplus-unofficial-documentation.readthedocs.org/) is an attempt to build robust, current documentation on the TinTin++ scripting language. The official documentation is much out of date, with new features being commonly used but completely undocumented (tables are a good example of this).

This documentation currently consists of @nfarrar's personal notes, with some input from [here](http://tintin.sourceforge.net/board/viewtopic.php?p=8797). Hoping that others (especially those with experience writing patches) may be willing to contribute some information.


Modules
-------
I've been working on methods of writing very portable, self-contained scripts for TinTin++, that can be shared among users. To achieve this end, several factors must be considered:

- The script configuration must be separated from the script purpose
- Scripts should have a way to verify that dependencies are met
- Scripts should be as self contained as possible
- Scripts should have some way to ensure that they don't interfere with each other (there is no scope)
- Scripts should be well tested
- Scripts should be well documented and adhere to a set of standards

I've started referring to these types of scripts/command files "modules" and been working on them on my own. I'm publishing my early, extremely alpha "modules" to this repository. Feel free to hack and test.


Source Code Mirror
------------------
@avidal maintains a mirror on github of the tintin++ source that has been added to the tintinplusplus organization. It is available [here](http://github.com/tintinplusplus/tintin).


IRC Channel
-----------
The unofficial TinTin++ IRC channel is <a href="irc://irc.freenode.net:6667/tintin">#tintin on freenode</a>. I started the channel some time ago and unfortunately it's been mostly dead since then, though there are a couple full-time idlers.


Contributors
------------
The following user's have contributed to the unofficial user's group projects:

- @nfarrar
- @avidal
