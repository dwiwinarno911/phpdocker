FROM phpdockerio/php7-fpm:latest

WORKDIR /application

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

# Install selected extensions and other stuff
RUN apt-get update \
    && apt-get -y --no-install-recommends install php7.0 php7.0-mysql php7.0-mcrypt php7.0-mbstring php7.0-cli php7.0-gd php7.0-curl php7.0-xml \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

RUN mkdir -p /var/cache/smarty/cache
RUN mkdir -p /var/cache/smarty/compile
RUN chmod -R 777 /var/cache/smarty

RUN usermod -u 1000 www-data && groupmod -g 1000 www-data