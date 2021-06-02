FROM php:8-fpm-alpine

RUN apk --no-cache update && apk --no-cache upgrade && \
  apk add --no-cache msmtp libzip-dev postgresql-dev zlib-dev libpng-dev \
    git imagemagick-dev && \
  ln -sf /usr/bin/msmtp /usr/sbin/sendmail && \
  git clone https://github.com/Imagick/imagick /usr/src/php/ext/imagick && \
  docker-php-ext-install pdo pdo_pgsql mysqli gd imagick exif zip 

