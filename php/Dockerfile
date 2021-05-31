FROM php:8-fpm

RUN apt-get update && \
  apt-get install -y msmtp libpq-dev zlib1g-dev libpng-dev && \
  apt-get clean && \
  ln -s /usr/bin/msmtp /usr/bin/sendmail && \
  docker-php-ext-install pdo pdo_pgsql mysqli gd

