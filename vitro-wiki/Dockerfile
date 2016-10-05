# nginx and php-fpm
FROM sotirk/nginx-php:1.0

MAINTAINER Kristian Sotiroff <kristians@gmail.com>

# INSTALL BITS
RUN apt-get update && apt-get install -y vim git

# bootstrapping
#RUN rm -v /etc/nginx/nginx.conf

# copy across tarball
RUN git clone https://gerrit.wikimedia.org/r/p/mediawiki/core.git /var/www/html

# add conf file from current dir
ADD nginx.conf /etc/nginx/

#append daemon off to from of file
RUN echo "daemon off;" >> /etc/nginx/nginx.conf

# Expose ports
EXPOSE 80

# Set the default command to execute
# when creating a new container
CMD service nginx start
