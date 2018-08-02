FROM dftlatam/docker-fpm-alpine:7.2

RUN set -xe \
  && apk update \
  && apk add --no-cache wget git \
  && wget https://pecl.php.net/get/xdebug \
  && tar -xf xdebug \
  && mkdir -p /usr/src/php/ext \
  && mv xdebug-* /usr/src/php/ext/xdebug \
  && docker-php-ext-install xdebug \
  && wget https://getcomposer.org/composer.phar \
  && mv composer.phar /usr/local/bin/composer \
  && chmod +x /usr/local/bin/composer \
  && apk del wget \
  
RUN set -xe \
  && apk --no-cache --update add \
  bzip2-dev \
  libpng-dev libwebp-dev libjpeg freetype-dev \
  gettext-dev \
  icu-dev \
  autoconf automake make gcc g++

RUN docker-php-ext-configure bcmath && \
  
#borrar
#  && docker-php-ext-configure bcmath --enable-bcmath \
#  && docker-php-ext-install gd memcached bcmath
#borrar
#  && rm -fr /usr/src/php/ext

