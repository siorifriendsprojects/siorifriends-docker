FROM php:7.1.6-fpm-alpine

LABEL maintainer "as-is-prog <as-is-prog@outlook.jp>"

# RUN apt-get update -y

# clean fpm conf
# RUN rm /usr/local/etc/php-fpm.d/*
COPY php-fpm.d /usr/local/etc/php-fpm.d
COPY php-conf/php.ini /usr/local/etc/php/

RUN mkdir -p /data
VOLUME ["/data"]
