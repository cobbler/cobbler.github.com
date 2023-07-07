---
layout: post
title: New Cobbler Home Page
author: James
summary: Welcome to the new Cobbler home page! The goal of this redesign is to make the website much more accessible, with documentation that's easier to find than digging through the github wiki. Going forward, there will be a manual for each major release (starting now with 2.2.3). This will allow us to provide documentation for users on older versions while maintaining updated docs for new releases (and maybe even the devel branch, as new features are added).
---

Welcome to the new Cobbler home page! The goal of this redesign is to make the website much more accessible, with
documentation that's easier to find than digging through the github wiki. Going forward, there will be a manual for each
major release (starting now with 2.2.3). This will allow us to provide documentation for users on older versions while
maintaining updated docs for new releases (and maybe even the devel branch, as new features are added).

Right now, the manual page is essentially a sorted hierarchy of of the wiki pages, with a LOT of holes in it. Not
everything has been given subsection numbers, so things are pretty jumbled. I'm continuing to work on this, and I hope
that by releasing this now others will start going through the manual pages and fixing things as well.

Want to get started? Clone the [cobbler.github.com](https://github.com/cobbler/cobbler.github.com) repo and start
sending pull requests! All you need installed is the jekyll ruby gem and python-pygments to test it out. Since github
runs their pages with jekyll's "safe mode" enabled, plugins don't work. This means you need to edit the .md files under
the \_dynamic/manuals directory and then run the generate_dynamic.sh script to compile everything into HTML files. This
script then rsyncs from \_dynamic/manuals/ to the root manuals/ directory. Run "git add" on that and commit.
