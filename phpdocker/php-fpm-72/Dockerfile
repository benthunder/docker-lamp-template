FROM phpdockerio/php72-fpm:latest
WORKDIR "/application"

# Fix debconf warnings upon build
ARG DEBIAN_FRONTEND=noninteractive

# Install selected extensions and other stuff
RUN apt-get update \
    && apt-get -y --no-install-recommends install  php-memcached php7.2-mysql php-redis php7.2-sqlite3 php-xdebug php7.2-bcmath php7.2-bz2 php7.2-gd php7.2-gmp php-imagick php7.2-intl php7.2-phpdbg php7.2-soap php-ssh2 php7.2-xmlrpc php-yaml php7.2-mbstring libapache2-mod-php7.2 \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*

COPY ./php-ini-overrides.ini /etc/php/7.2/fpm/conf.d/99-overrides.ini