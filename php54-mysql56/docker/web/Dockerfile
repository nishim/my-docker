FROM php:5.4-apache

RUN apt-get update
RUN docker-php-ext-install mbstring
RUN docker-php-ext-install mysql
RUN docker-php-ext-install json
RUN docker-php-ext-install iconv
RUN apt-get install -y libmcrypt-dev
RUN docker-php-ext-install mcrypt
RUN pecl channel-update pecl.php.net
RUN pecl install xdebug-2.4.1
RUN docker-php-ext-enable xdebug
COPY php.ini /usr/local/etc/php/php.ini

RUN curl -sSLO https://github.com/mailhog/mhsendmail/releases/download/v0.2.0/mhsendmail_linux_amd64 \
    && chmod +x mhsendmail_linux_amd64 \
    && mv mhsendmail_linux_amd64 /usr/local/bin/mhsendmail