FROM php:7.4-fpm-alpine

RUN apk update && apk add --no-cache \
    $PHPIZE_DEPS \
    && pecl install redis \
    && docker-php-ext-enable redis  \
    && docker-php-ext-install pdo_mysql pcntl

WORKDIR /var/www

CMD ["php-fpm"]
