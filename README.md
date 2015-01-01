[tldrcode.com](http://tldrcode.com)
============
[![Gitter](https://badges.gitter.im/Join Chat.svg)](https://gitter.im/tldrcode/tldrcode.com?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![TravisCI Status](https://travis-ci.org/tldrcode/tldrcode.com.svg)](https://travis-ci.org/tldrcode/tldrcode.com)

Don't waste time with syntax; unleash the code!

## About
After learning the concepts behind programming, learning a new language comes
down to one thing: syntax. The goal of tl;dr{code} is to be a central hub for
programming syntax, allowing developers to focus more on the code itself.

Contributions
-------------
For those looking to contribute, this section is for you! We need people like you to keep this site accurate and up-to-date. Below is a list of ways you can personally contribute to the project.

- Submit Issues to our Issue Tracker
- Correct Issues in our Issue Tracker
- Add a new Language
- Correct/expand existing languages
- Create site documentation
- Send us pull requests
  - New features
  - Fix our existing features

If you can do any of the above we will be eternally grateful.

## Running Locally with Vagrant
If you want to run a local version of the tl;dr{code} with vagrant, install
[vagrant](https://www.vagrantup.com/) and change to the tldrcode.com project directory. Follow these instructions -

    vagrant up
    # This command is run automatically by the Vagrant provisioner whenever the
    # machine comes up, no need to do this manually
    cd /vagrant; jekyll server --watch -P 8080 --force_polling

There is a vagrantfile preconfigured in the project directory.

If you want to run the same `HTML-Proofer` we run for Travis-CI in the vagrant
box -

    vagrant ssh
    cd /vagrant
    htmlproof ./_site --href_ignore "#"

FAQ
---
Q. Why are the language files named `*.markdown` and only contain YAML?

A. They are `.markdown` files because Jekyll will not render a page from a `.yml` file. Jekyll does allow for rendering of a `.markdown` files into multiple pages. The key is that the Markdown files can contain a YAML front matter. We exploit this ability by only having a YAML front matter and nothing in markdown.

## Site Colors
- Dark Gray: #2a2a2a
- Light Gray: #646464
- Pink: #de577b
- Mint: #3fa38d
- Off White: #edeff0
