FROM php:8-fpm

RUN apt-get update && \
  apt-get install -y msmtp libpq-dev zlib1g-dev libpng-dev \
    git libmagickwand-dev && \
  apt-get clean && \
  ln -s /usr/bin/msmtp /usr/sbin/sendmail && \
  git clone https://github.com/Imagick/imagick /usr/src/php/ext/imagick && \
  docker-php-ext-install pdo pdo_pgsql mysqli gd imagick && \
  apt remove -y git libmagickwand-dev && apt clean

