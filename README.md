# Deha-Academy-Docker-Lap1 - Bài Lab Docker

Bài lab này bao g?m các b??c th?c hành c? b?n ?? làm quen v?i Docker, Docker Image, Docker Container, Dockerfile và Docker Compose, c?ng nh? cách s? d?ng Laradock ?? t?o môi tr??ng phát tri?n cho ?ng d?ng PHP (Laravel).

## Các b??c ?ã th?c hi?n:

1.  **Chu?n b? môi tr??ng:**
    * ?ã cài ??t Docker Desktop.
2.  **T?o Repository Git:**
    * ?ã t?o repository tên `Deha-Academy-Docker-Lap1` trên Git.
    * ?ã sao chép URL c?a repository.

3.  **Clone Repository v? Máy Tính:**
    * ?ã clone repository v? th? m?c `E:/Deha-Academy-Docker-Lap1`.

4.  **Các câu l?nh Docker c? b?n:**
    * ?ã ch?y và ghi l?i output c?a các l?nh: `docker login`, `docker logout`, `docker version` vào file `docker-commands.md`.

5.  **Các câu l?nh v?i Docker Image:**
    * ?ã ch?y và ghi l?i output c?a các l?nh: `docker pull nginx:latest`, `docker image ls`, `docker tag`, `docker push`, `docker rmi` vào file `docker-commands.md`.

6.  **Các câu l?nh v?i Docker Container:**
    * ?ã ch?y và ghi l?i output c?a các l?nh liên quan ??n container (`docker run`, `docker ps`, `docker ps -a`, `docker exec`, `docker stop`, `docker start`, `docker rm`) vào file `docker-container-commands.md`.

7.  **S? d?ng Docker image và Docker Compose t?o môi tr??ng ch?y ?ng d?ng PHP:**
    * ?ã t?o th? m?c `my-php-app` và c?u trúc th? m?c bên trong (`app`, `docker/nginx/conf`, `docker/php`, `docker/mysql`).
    * ?ã t?o file `index.php` ??n gi?n.
    * ?ã t?o các file `Dockerfile` cho Nginx, PHP, MySQL.
    * ?ã t?o file `default.conf` cho Nginx.
    * ?ã t?o file `docker-compose.yml` ?? ??nh ngh?a các service.
    * ?ã th? kh?i ch?y môi tr??ng PHP b?ng `docker-compose up -d --build`

8.  **Thay ??i c?u hình Docker Compose:**
    * ?ã ch?nh s?a file `docker-compose.yml` trong th? m?c `my-php-app` ?? thay ??i tên và port c?a các service.
    * ?ã ch?y l?i `docker-compose up -d --force-recreate --build` ?? áp d?ng thay ??i
    * ?ã t?o file `docker-compose-config.md` và ghi l?i các thay ??i trong `docker-compose.yml`.

9.  **S? d?ng Laradock t?o môi tr??ng ch?y Laravel:**
    * ?ã t?o th? m?c `Laradock` trong `E:/Deha-Academy-Docker-Lap1`.
    * ?ã clone repository Laradock vào th? m?c `Laradock`.
    * ?ã sao chép và ch?nh s?a file `.env` c?a Laradock ?? c?u hình `PHP_VERSION`, `NGINX_HOST_HTTP_PORT`, `MYSQL_VERSION`, và `APP_CODE_PATH_HOST`.
    * ?ã t?o th? m?c `laravel` ngang hàng v?i th? m?c `Laradock`.
    * **Tr?ng thái kh?i ch?y Laradock:** [Ch?y l?nh `docker compose up -d nginx php-fpm` ch?a thành công do dung l??ng ? C máy tính không ??, ?ã cài ??t l?i nhi?u l?n vào ? E nh?ng Docker Desktop t? nh? c?u hình vào ? C].

## Các file ?ã t?o:

* `docker-commands.md`
* `docker-container-commands.md`
* `my-php-app/` (và các file bên trong)
* `my-php-app/docker-compose.yml`
* `my-php-app/docker-compose-config.md`
* `Laradock/` (và các file bên trong)
* `Laradock/.env`
* `laravel/` 

## Các thay ??i trong file `.env` c?a Laradock:
PHP_VERSION=8.1
 NGINX_HOST_HTTP_PORT=8000
 MYSQL_VERSION=5.7
 APP_CODE_PATH_HOST=../laravel/

