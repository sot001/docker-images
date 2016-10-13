# jekyll
FROM jekyll/jekyll:latest

MAINTAINER Kristian Sotiroff <kristians@gmail.com>

# INSTALL BITS
#RUN gem install jekyll bundler

# bootstrapping
VOLUME /srv/jekyll/

# clone in site
#RUN git clone https://gerrit.wikimedia.org/r/p/mediawiki/core.git /var/www/mediawiki

# Set the default command to execute
CMD jekyll serve -s /srv/jekyll/pindan-wiki/
