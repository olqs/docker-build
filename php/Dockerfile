FROM php:8-fpm-alpine

RUN apk update && apk upgrade && \
  apk add msmtp libzip-dev postgresql-dev zlib-dev libpng-dev \
    git imagemagick-dev && \
  apk cache clean && \
  ln -s /usr/bin/msmtp /usr/sbin/sendmail && \
  git clone https://github.com/Imagick/imagick /usr/src/php/ext/imagick && \
  docker-php-ext-install pdo pdo_pgsql mysqli gd imagick exif zip 

