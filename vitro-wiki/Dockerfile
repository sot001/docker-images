# nginx and php-fpm
FROM sotirk/nginx-php:latest

MAINTAINER Kristian Sotiroff <kristians@gmail.com>

# INSTALL BITS
RUN apt-get update && apt-get install -y vim git

# bootstrapping
# get rid of original conf file
#RUN rm -v /etc/nginx/nginx.conf

# stick ours in
#COPY nginx.conf /etc/nginx/nginx.conf

# copy across tarball
RUN git clone https://gerrit.wikimedia.org/r/p/mediawiki/core.git /var/www/mediawiki

# swap from socket to port
RUN sed -i 's\listen = /run/php/php7.0-fpm.sock\listen = 127.0.0.1:9000;\g' /etc/php/7.0/fpm/pool.d/www.conf

# add wiki conf file 
ADD wiki.conf /etc/nginx/conf.d/wiki.conf

# append daemon off to end of file
RUN echo "daemon off;" >> /etc/nginx/nginx.conf

# Set the default command to execute
CMD service php7.0-fpm start && nginx
