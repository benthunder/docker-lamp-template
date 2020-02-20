FROM nginx:stable

ARG DEBIAN_FRONTEND=noninteractive

# Install vim
RUN apt-get update \
    && apt-get install -y \
        vim

COPY ./nginx.conf /etc/nginx/conf.d/default.conf
COPY ./site.wordpress.conf /etc/nginx/conf.d/wordpressdemo.local.conf 
COPY ./site.laravel.conf /etc/nginx/conf.d/laraveldemo.local.conf 