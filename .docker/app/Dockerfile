FROM phpearth/php:7.3-apache

COPY app /

RUN apk add --no-cache php7.3-pdo php7.3-pdo_mysql php7.3-pear php7.3-gd \
    make composer \
    && cp /etc/php/7.3/php.ini-development /etc/php/7.3/php.ini \
    # Increase upload file size to 20MB (application limits it to 16MB)
    && echo "upload_max_filesize = 20M" >> /etc/php/7.3/php.ini \
    && echo "post_max_size = 22M" >> /etc/php/7.3/php.ini

WORKDIR /var/www/app
