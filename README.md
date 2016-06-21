# XMPP Site Source


## Jekyll

[Jekyll](http://jekyllrb.com/) is a static site generator built in [Ruby on Rails](http://rubyonrails.org/). With this approach, you are able to build a high power build site, using a low power, very stable webserver running a static site.

Jekyll is not needed on the webserver, updates must be done by a build system, from this source repository, then sent to the webserver.

### Updating the site

First change into the source directory of the site, once in, update via

    jekyll build

A simple script would be

    rm -rf /var/src/im.mattrude.com && mkdir -p /var/src/ && \
    git clone git@github.com:mattrude/im.mattrude.com.git /var/src/im.mattrude.com -q && \
    cd /var/src/im.mattrude.com && jekyll build -q && rm -rf /var/src/im.mattrude.com

## Installing the server

### Nginx Configuration

    #----------------------------------------------------------------------
    # mattrude.com XMPP Service
    #----------------------------------------------------------------------

    # im.mattrude.com
    server {
        listen 80;
        listen [::]:80;
        listen <set your IP>11371;
        listen [set your IPv6 IP]:11371;
        server_name im.mattrude.com;
        root /var/www/im.mattrude.com;
    }


### Installing Jekyll
Since Jekyll only needs to be installed on your build system. Below are a few quick how-to's how setting up your build system.

#### Installing Ruby on Ubuntu
On Ubuntu 14.04 LTS, you first need ruby installed on your setup, we will also install the development kit.

    apt-get update; apt-get install -y git g++ ruby ruby-dev

Next install the needed gems and Jekyll

    gem install rails
    gem install rouge
    gem install kramdown
    gem install therubyracer
    gem install jekyll
    gem install jekyll-press
    gem install jekyll-sitemap
    gem install jekyll-less
    gem install jekyll-redirect-from
    gem install jekyll-last-modified-at

Now you may use Jekyll to build the site, using the source provided in this repository.

#### Installing Ruby on Windows
First start out by downloading the current production version of the [Ruby Installer](http://rubyinstaller.org/downloads/) for windows.

##### Installing the Ruby Development Kit
After installing Ruby via the [Ruby Installer](http://rubyinstaller.org/downloads/) talked about above, you must now download the Development Kit.

1. Download the Development Kit from http://rubyinstaller.org/downloads/
1. Extract the contact into a location easy accessible to your command prompt.
1. Open a command prompt, change into the directory that you extracted the content of the Development Kit to and run the command: `rake devkit sfx=1`.

## License

                  GNU GENERAL PUBLIC LICENSE
                    Version 3, 29 June 2007

    mattrude.com XMPP Service Website for im.mattrude.com
    Copyright (C) 2012-2016 Matt Rude <matt@mattrude.com>

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.
