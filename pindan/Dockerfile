# jekyll
#FROM jekyll/jekyll:latest
FROM sotirk/pindan:v1

MAINTAINER Kristian Sotiroff <kristians@gmail.com>

# INSTALL BITS
#RUN gem install jekyll bundler

# bootstrapping
RUN cd /srv/jekyll/pindan/

# clone in site
#RUN git clone https://gerrit.wikimedia.org/r/p/mediawiki/core.git /var/www/mediawiki

# Set the default command to execute
CMD bundle exec jekyll serve
