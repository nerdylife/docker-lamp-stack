FROM php:7.2-apache
COPY php.ini /usr/local/etc/php/
COPY 000-default.conf /etc/apache2/sites-available/

RUN apt-get update \
	&& apt-get install -y curl libfreetype6-dev libjpeg62-turbo-dev libmcrypt-dev libzip-dev \
	&& docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
	&& docker-php-ext-install pdo_mysql mysqli mbstring gd iconv

RUN	pecl install xdebug zip \
	&& docker-php-ext-enable xdebug zip
