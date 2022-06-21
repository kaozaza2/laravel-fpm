ENV PHP_VERSION

FROM php:$PHP_VERSION-fpm

RUN docker-php-ext-install bcmath pdo_mysql

WORKDIR /var/www/html

EXPOSE 9000

CMD ["php-fpm"]
