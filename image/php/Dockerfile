FROM php:7.2-fpm

RUN apt-get update && apt-get install -y zip unzip \
    git \
    libmcrypt-dev \
    libpq-dev \
    && docker-php-ext-install pdo_mysql

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www/html

ADD ./src /var/www/html
