FROM php:8.1-fpm
WORKDIR /application
ARG DEBIAN_FRONTEND=noninteractive
#--------------------------------------------------------------------------
# Install requirements packages
#-------------------------------------------------------------------------

RUN echo 'deb [trusted=yes] https://repo.symfony.com/apt/ /' |  tee /etc/apt/sources.list.d/symfony-cli.list
RUN apt update

RUN  apt-get install  -y  zip  grep libpng-dev wget  bash curl libzip-dev libyaml-dev  symfony-cli graphviz

RUN docker-php-source extract \
    && docker-php-ext-install pdo pdo_mysql gd zip \
    && docker-php-source delete \
    && docker-php-ext-install mysqli && docker-php-ext-enable mysqli 

RUN pear channel-update pear.php.net
RUN pecl channel-update pecl.php.net

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN curl -LS https://github.com/qossmic/deptrac/releases/download/0.19.3/deptrac.phar -o deptrac.phar
RUN chmod +x deptrac.phar
RUN mv deptrac.phar /usr/local/bin/deptrac


RUN usermod -u 1000 www-data && groupmod -g 1000 www-data