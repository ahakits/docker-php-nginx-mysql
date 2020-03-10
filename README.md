# docker-php-nginx-mysql

Local Development Environment for PHP using Docker for Mac.

## Requirement

- Docker for Mac

## Usage

1. `docker-compose up -d --build`
2. deploy your application to `./php/application`
3. edit `./php/application/compose.json`
4. `docker-compose run composer install`


* If you want to use Xdebug for Remote debug, change Debug port to `9001`.
* If you want to test by PHPUnit, use `cli` service.
