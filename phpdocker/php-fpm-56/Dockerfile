FROM phpdockerio/php56-fpm:latest
WORKDIR "/application"

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

# Install selected extensions and other stuff
RUN apt-get update \
    && apt-get -y --no-install-recommends install  php5-memcached php5-mysql php5-redis php5-sqlite php5-gd php5-gmp php5-imagick php5-memcache php5-oauth php5-phpdbg php5-ssh2 php5-solr php5-xdebug \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

COPY ./php-ini-overrides.ini /etc/php/7.2/fpm/conf.d/99-overrides.ini