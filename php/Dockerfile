FROM php:8-fpm

RUN apt-get update && \
  apt-get install -y msmtp libzip-dev libpq-dev zlib1g-dev libpng-dev \
    git libmagickwand-dev libmagickcore-6.q16-6-extra libjpeg62-turbo-dev && \
  apt-get clean && \
  ln -s /usr/bin/msmtp /usr/sbin/sendmail && \
  git clone https://github.com/Imagick/imagick /usr/src/php/ext/imagick && \
  docker-php-ext-configure gd --with-jpeg && \
  docker-php-ext-install pdo pdo_pgsql mysqli gd imagick exif zip && \
  apt-get remove -y git libmagickwand-dev && \
  apt-get -y autoremove && \
  apt-get clean

