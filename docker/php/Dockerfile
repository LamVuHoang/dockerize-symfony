FROM php:8.1-fpm-alpine

WORKDIR /var/www/html

# COPY src .

# 
RUN set -ex \
  && apk --no-cache add \
    postgresql-dev

RUN docker-php-ext-install pdo pdo_pgsql

RUN addgroup -g 1000 symfony && adduser -G symfony -g symfony -s /bin/sh -D symfony

USER symfony

# RUN chown -R symfony:symfony .

# www-data is the default user:group created by php:7.4-fpm-alpine image
# RUN chown -R www-data:www-data /var/www/html