FROM dftlatam/docker-fpm-alpine:7.2
RUN apk update \
    && mkdir -p /usr/src/php/ext \
    && docker-php-ext-install bcmath \
    && docker-php-ext-enable bcmath \
    && rm -fr /usr/src/php/ext

ONBUILD COPY . /var/www/html
