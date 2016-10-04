# nginx and php-fpm
FROM ubuntu:16.04

MAINTAINER Kristian Sotiroff <kristians@gmail.com>

# INSTALL BITS
RUN apt-get update && apt-get install -y nginx php-fpm fcgiwrap vim

# bootstrapping
RUN rm -v /etc/nginx/nginx.conf

# add conf file from current dir
ADD nginx.conf /etc/nginx/

#append daemon off to from of file
RUN echo "daemon off;" >> /etc/nginx/nginx.conf

# Expose ports
EXPOSE 80

# Set the default command to execute
# when creating a new container
CMD service nginx start
