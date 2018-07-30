FROM dftlatam/docker-fpm-alpine:7.2
RUN apk update \
    && docker-php-ext-install bcmath \
    && docker-php-ext-enable bcmath

ONBUILD COPY . /var/www/html
