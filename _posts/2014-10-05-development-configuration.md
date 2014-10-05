---
layout: post
title:  Submodule Configuration
author: nfarrar
categories: development
---
The tintinplusplus repositories are all individual. I find that for development purposes, it's very convenient to map all this content & code into a single directory structure - and that the best way (I know of) to do this, is by adding them as submodules to my existing 'mudfiles' project. The following is how I set it all up.

First, I clone my mudfiles:

    MUDFILES="$HOME/Documents/Projects/Mudfiles"
    git clone https://github.com/nfarrar/tintin-nannymud $MUDFILES
    cd $MUDFILES

Next, I add the tintinplus repositories as submodules:

    git submodule add git@github.com:tintinplusplus/tintinplusplus-unoffical-documentation.git docs
    git submodule add git@github.com:tintinplusplus/tintinplusplus-modules.git share
    git submodule add git@github.com:tintinplusplus/tintin.git tintin
    git submodule add git@github.com:tintinplusplus/tintinplusplus.github.io.git website

And setup branch tracking for each submodule (without this, you'll constantly end up with submodules in a detached head state):

    git config -f .gitmodules submodule.docs.branch master
    git config -f .gitmodules submodule.share.branch master
    git config -f .gitmodules submodule.tintin.branch master
    git config -f .gitmodules submodule.website.branch master
    git config -f .gitmodules submodule.srv.branch master

My system wide git configuration ($HOME/.gitconfig) has the following configuration set:

    pull.rebase=true
    rerere.enabled=true

Which affects the behavior of the following commands. These commands make sure that each submodule has the master branch checked out, and in conjunction with the previous configuration setup the default pull and rebase behavior:

    pushd docs && git branch -u origin/master master && popd
    pushd share && git branch -u origin/master master && popd
    pushd tintin && git branch -u origin/master master && popd
    pushd website && git branch -u origin/master master && popd

Finally, I commit the .gitmodules file to my base repository and push it origin, setting it as my default upstream:

    git add .gitmodules
    git commit .gitmodules -m 'added submodules'
    git push -u origin master


Now everything stays in sync nicely.