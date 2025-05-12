# --- Stage build cho Composer ---
FROM composer:latest AS composer
WORKDIR /app
RUN mkdir -p /app  # Đảm bảo thư mục /app tồn tại
COPY ./app/composer.json /app/composer.json
COPY ./app/composer.lock /app/composer.lock
RUN composer install --no-dev --optimize-autoloader --ignore-platform-reqs