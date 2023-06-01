FROM nginx:stable-alpine

WORKDIR /etc/nginx/conf.d

COPY docker/nginx_symfony/nginx.conf .

RUN mv nginx.conf default.conf

WORKDIR /var/www/html

# COPY src .