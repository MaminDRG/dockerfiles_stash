FROM php:7.1-fpm
RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg-dev \
        libjpeg62-turbo-dev \
        libxpm-dev \
        libvpx-dev \
        libmcrypt-dev \
        libpng-dev \
        libicu-dev \
        libpq-dev \
    && docker-php-ext-install gd pdo pdo_mysql pdo_pgsql intl zip bcmath pcntl sysvmsg exif \
    && docker-php-ext-configure gd \
    --with-freetype-dir=/usr/include/ \
    --with-jpeg-dir=/usr/include/ 

USER nobody
