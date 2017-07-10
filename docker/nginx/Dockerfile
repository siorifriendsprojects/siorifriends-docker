FROM nginx:1.12.0-alpine

LABEL maintainer "as-is-prog <as-is-prog@outlook.jp>"

RUN set -x ; \
  addgroup -g 82 -S www-data ; \
  adduser -u 82 -D -S -G www-data www-data && exit 0 ; exit 1

COPY config/nginx_run.sh /run/nginx_run.sh
RUN chmod +x /run/nginx_run.sh
COPY config/nginx.conf /etc/nginx/nginx.conf
COPY config/laravel.conf /etc/nginx/conf.d/laravel.conf
RUN rm /etc/nginx/conf.d/default.conf

RUN mkdir -p /data
VOLUME ["/data"]

#CMD ["/run/nginx_run.sh"]
