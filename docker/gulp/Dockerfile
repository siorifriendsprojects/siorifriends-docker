FROM debian:jessie

LABEL maintainer "as-is-prog <as-is-prog@outlook.jp>"

RUN apt-get update -y
RUN apt-get install -y curl git
# RUN curl -sL https://deb.nodesource.com/setup | bash --
RUN apt-get install -y nodejs
RUN apt-get install -y npm
RUN npm update -g npm
RUN npm cache clean
RUN npm i -g n
RUN n stable
RUN apt-get purge -y nodejs npm
RUN npm i -g gulp-cli

RUN mkdir -p /data/www
VOLUME ["/data"]
WORKDIR /data/www

ENTRYPOINT ["gulp"]
CMD ["-h"]
