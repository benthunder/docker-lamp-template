FROM httpd:2.4

ARG DEBIAN_FRONTEND=noninteractive

# Install vim
RUN apt-get update \
    && apt-get install -y \
        vim

RUN mkdir /usr/local/apache2/sites-available
RUN chmod -R 0775 /usr/local/apache2/sites-available

COPY ./vhost.conf /usr/local/apache2/conf/extra/vhost.conf
