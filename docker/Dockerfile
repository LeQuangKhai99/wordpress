FROM wordpress:php8.2-fpm

COPY --from=composer /usr/bin/composer /usr/bin/composer

COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/local/bin/

RUN install-php-extensions gd pdo_mysql mysqli redis imagick zip

WORKDIR /var/www/html/wp/

EXPOSE 9000