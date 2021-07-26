FROM php:7.4-fpm
RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libpng-dev \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install -j$(nproc) gd

#PDOのMySQLドライバーをインストール
RUN docker-php-ext-install pdo_mysql
#composer を入れる
COPY --from=composer /usr/bin/composer /usr/bin/composer

#xdebugを入れとく
RUN pecl install xdebug \
  && docker-php-ext-enable xdebug