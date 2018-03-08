FROM php:7.2-fpm

COPY php.ini $PHP_INI_DIR/conf.d/

RUN apt-get update

# Install PDO
RUN docker-php-ext-install pdo_mysql

# Install mbstring
RUN docker-php-ext-install mbstring

