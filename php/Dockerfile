FROM php:7.2-fpm

COPY php.ini $PHP_INI_DIR/conf.d/

RUN apt-get update && \
        docker-php-source extract && \
        docker-php-ext-install pdo_mysql mbstring

# Pecl Install
RUN pecl install redis xdebug && \
        docker-php-ext-enable redis xdebug

RUN rm -rf /tmp/pear

WORKDIR /var/www/html
COPY application/ /var/www/html/

