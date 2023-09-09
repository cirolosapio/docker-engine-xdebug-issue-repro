FROM php:8.1.22-fpm-alpine3.18

RUN apk --no-cache add autoconf make g++ linux-headers
RUN pecl install xdebug
RUN docker-php-ext-enable xdebug
