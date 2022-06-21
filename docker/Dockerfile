ARG PHP_VERSION

FROM php:$PHP_VERSION-fpm

# Install required extenstions
RUN docker-php-ext-install bcmath pdo_mysql

# Install composer
RUN apt-get update \
    && apt-get install zip unzip -y \
    && php -r "readfile('https://getcomposer.org/installer');" | php -- --install-dir=/usr/bin/ --filename=composer

# Install nodejs & yarn
RUN curl -sLS https://deb.nodesource.com/setup_16.x | bash - \
    && apt-get install -y nodejs \
    && npm install --location=global npm \
    && npm install --location=global yarn
