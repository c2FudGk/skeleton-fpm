FROM php:7.4-fpm

WORKDIR /var/www

ENV PHP_IDE_CONFIG "serverName=santi"

RUN apt-get update && apt-get install -y \
    zip \
    unzip \
    git \
    vim

RUN printf "\n" | pecl install -f xdebug-2.9.5

RUN docker-php-ext-install bcmath

RUN docker-php-ext-enable xdebug

RUN curl --insecure https://getcomposer.org/composer.phar -o /usr/bin/composer && chmod +x /usr/bin/composer

COPY xdebug.ini /usr/local/etc/php/conf.d/xdebug.ini
