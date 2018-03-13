FROM php:7.2-fpm

COPY php.ini $PHP_INI_DIR/conf.d/

RUN apt-get update
RUN docker-php-source extract

# Install PDO
RUN docker-php-ext-install pdo_mysql

# Install mbstring
RUN docker-php-ext-install mbstring

# Install redis
RUN pecl install redis && \
        docker-php-ext-enable redis

# Install xdebug
RUN pecl install xdebug && \
        docker-php-ext-enable xdebug

RUN rm -rf /tmp/pear
