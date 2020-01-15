FROM php:7.2-apache
RUN apt-get update
RUN docker-php-ext-install pdo pdo_mysql mysqli
#Core Ext
RUN apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libpng-dev

#PECL Ext
RUN pecl install redis-5.1.1 \
    && pecl install xdebug-2.7.1 \
    && docker-php-ext-enable redis xdebug
RUN a2enmod rewrite