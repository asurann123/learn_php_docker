#php:8.0-apacheでも動くことを確認済み
FROM php:7.4-apache

#PDOのMySQLドライバーをインストール
RUN docker-php-ext-install pdo_mysql

#xdebugを入れとく
RUN pecl install xdebug \
  && docker-php-ext-enable xdebug