FROM php:7.1.6-fpm-alpine

LABEL maintainer "as-is-prog <as-is-prog@outlook.jp>"

RUN docker-php-ext-install mysqli pdo pdo_mysql

#COPY php-fpm.d /usr/local/etc/php-fpm.d
#COPY php-conf/php.ini /usr/local/etc/php/

RUN mkdir -p /data/www
VOLUME ["/data"]
WORKDIR /data/www

ENTRYPOINT ["php","artisan"]
CMD ["--help"]
