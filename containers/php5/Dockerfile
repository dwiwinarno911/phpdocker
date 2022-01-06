FROM phpdockerio/php56-fpm:latest

WORKDIR /application

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

# Install selected extensions and other stuff
RUN apt-get update \
    && apt-get -y --no-install-recommends install  php5-mysql php5-gd php5-xdebug php5-xmlrpc \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

RUN mkdir -p /var/cache/smarty/cache
RUN mkdir -p /var/cache/smarty/compile
RUN chmod -R 777 /var/cache/smarty

RUN usermod -u 1000 www-data && groupmod -g 1000 www-data