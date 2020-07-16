FROM php:7.4-fpm

LABEL maintainer="gonyamagon@gmail.com"

RUN apt-get update && apt-get install -y \
    git vim unzip \
    && docker-php-ext-install pdo_mysql \
    && apt-get clean

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

ENV CURRENT_DIR /var/www/app

WORKDIR $CURRENT_DIR
