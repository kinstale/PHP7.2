FROM php:7.2-fpm-alpine

RUN docker-php-ext-install -j$(nproc) mysqli opcache

ADD php.ini /usr/local/etc/php.ini 
