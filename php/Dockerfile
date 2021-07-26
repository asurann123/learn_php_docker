#php:8.0-apacheでも動くことを確認済み
FROM php:7.4-apache

# おまじない
RUN apt update -y
RUN apt install git -y

#PDOのMySQLドライバーをインストール
RUN docker-php-ext-install pdo_mysql

#composer を入れる
COPY --from=composer /usr/bin/composer /usr/bin/composer

#xdebugを入れとく
RUN pecl install xdebug \
  && docker-php-ext-enable xdebug