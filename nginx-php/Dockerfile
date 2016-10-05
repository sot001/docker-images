# nginx, fgiwrap and php-fpm
FROM ubuntu:16.04

MAINTAINER Kristian Sotiroff <kristians@gmail.com>

# INSTALL BITS
RUN apt-get update && apt-get install -y nginx php-fpm fcgiwrap

#append daemon off to from of file
RUN echo "daemon off;" >> /etc/nginx/nginx.conf

# Expose ports
EXPOSE 80 443

# Set the default command to execute
# when creating a new container
CMD service nginx start
