FROM httpd:2.4

ARG DEBIAN_FRONTEND=noninteractive

# Install vim
RUN apt-get update \
    && apt-get install -y \
        vim

# COPY ./nginx.conf /etc/nginx/conf.d/default.conf