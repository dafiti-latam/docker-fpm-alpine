FROM dftlatam/docker-fpm-alpine:7.2-test-frank

# AMQP
RUN echo http://dl-cdn.alpinelinux.org/alpine/v3.6/main >> /etc/apk/repositories
RUN apk update
RUN apk --no-cache --update add rabbitmq-c-dev
RUN pecl install amqp
RUN docker-php-ext-enable amqp
# Cleanup
RUN rm -rf /tmp/* && rm -rf /var/cache/apk/*

#borrar
#  && docker-php-ext-configure bcmath --enable-bcmath \
#  && docker-php-ext-install gd memcached bcmath
#borrar
#  && rm -fr /usr/src/php/ext
