# Frontend Performance Training

This repo contains slides and materials to help you learn about frontend performance. From basic principles to workflow automation, you and your team can learn how to audit sites, fix problems, and stick to a performance budget throughout the life of a project.

## Learning Objectives

- **Create a foundation of knowledge** which allows you to optimize an existing site.
- **Confidently build a performant site** from scratch while balancing other priorities like feature backlogs and deadlines.
- **Use automated workflow tools** to check every change you make to a site, ensuring that major changes in performance do not go unnoticed during the development cycle.

## History

* [DrupalCon LA 2015](https://events.drupal.org/losangeles2015/training/frontend-performance-training)
* [DrupalCon Barcelona 2015](https://events.drupal.org/barcelona2015/training/frontend-performance-training)

# Installation

This repo uses Ruby and npm to power a Jekyll site. Assuming you already have [Homebrew](http://brew.sh/), the following commands will install the whole training kit for you (run them at the root of the repo).

# NOTE: NEVER USE `sudo` TO INSTALL!

## OS X

```
# update homebrew
brew update

# install node version manager the specific version
# of node.js needed by these training materials
brew install nvm
nvm install v0.12.7
nvm use

# install rbenv
brew install rbenv
brew install ruby-build

# install ruby
rbenv install 2.0.0-p451

# install the rest of the tools
gem install bundler
bundle install
npm install -g gulp
npm install

# run the development server
gulp bs
```

## Debian/Ubuntu

```
# update repositories
sudo apt-get update

# check for old node package
dpkg --get-selections | grep node

# if old node package installation found by previous command,
# we recommend removing it to avoid name collisions
sudo apt-get remove --purge node

# install nvm (the Node version manager)
# See https://github.com/creationix/nvm#install-script
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.31.0/install.sh | bash

# install the version of node used in these examples
# if "nvm: command not found" error, close and reopen your terminal or session
nvm install v0.12.7
nvm use

# install rvm
\curl -sSL https://get.rvm.io | bash -s stable --rails
source ~/.rvm/scripts/rvm

# install ruby
rvm install ruby-2.0.0-p451
gem install bundler

# install the rest of the tools
cd path/to/this/repo
bundle install
npm install -g gulp
npm install

# run the development server
gulp bs
```

## Windows

Unfortunately at this time we do not have detailed, reliable installation instructions for local Windows development. We recommend using a linux VM for development, and your preferred Windows IDE to edit files.
