FROM nginx:stable-alpine

LABEL maintainer="Manuel Portillo <manuel220@gmail.com>"

RUN apk add --no-cache --update --virtual .supervisord  supervisor && \
    apk add --no-cache --update --virtual .php --update php7 php7-fpm

COPY php-fpm-www.conf /etc/php7/php-fpm.d/www.conf
COPY supervisord.conf /etc/supervisord.conf
COPY default /etc/nginx/conf.d/default.conf
COPY web/ /var/www/app/web/

ENTRYPOINT ["supervisord", "--configuration", "/etc/supervisord.conf"]