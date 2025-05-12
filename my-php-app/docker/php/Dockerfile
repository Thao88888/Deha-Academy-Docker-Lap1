FROM php:8.1-fpm-alpine AS base

# Cài đặt các extension PHP cần thiết
RUN apk add --no-cache --update $PHPIZE_DEPS \
    && docker-php-ext-install pdo pdo_mysql mysqli

WORKDIR /var/www/html

# Sao chép mã nguồn ứng dụng
COPY ./app /var/www/html

# Chuyển sang user không phải root
USER www-data

EXPOSE 9000

CMD ["php-fpm"]

# --- Stage build cho Composer ---
FROM composer:latest AS composer
WORKDIR /app
RUN mkdir -p /app
COPY ./app/composer.json /app/composer.json
COPY ./app/composer.lock /app/composer.lock
RUN composer install --no-dev --optimize-autoloader --ignore-platform-reqs

# --- Final Image ---
FROM base
COPY --from=composer /app/vendor /var/www/html/vendor