# Deha-Academy-Docker-Lap1 - B�i Lab Docker

B�i lab n�y bao g?m c�c b??c th?c h�nh c? b?n ?? l�m quen v?i Docker, Docker Image, Docker Container, Dockerfile v� Docker Compose, c?ng nh? c�ch s? d?ng Laradock ?? t?o m�i tr??ng ph�t tri?n cho ?ng d?ng PHP (Laravel).

## C�c b??c ?� th?c hi?n:

1.  **Chu?n b? m�i tr??ng:**
    * ?� c�i ??t Docker Desktop.
2.  **T?o Repository Git:**
    * ?� t?o repository t�n `Deha-Academy-Docker-Lap1` tr�n Git.
    * ?� sao ch�p URL c?a repository.

3.  **Clone Repository v? M�y T�nh:**
    * ?� clone repository v? th? m?c `E:/Deha-Academy-Docker-Lap1`.

4.  **C�c c�u l?nh Docker c? b?n:**
    * ?� ch?y v� ghi l?i output c?a c�c l?nh: `docker login`, `docker logout`, `docker version` v�o file `docker-commands.md`.

5.  **C�c c�u l?nh v?i Docker Image:**
    * ?� ch?y v� ghi l?i output c?a c�c l?nh: `docker pull nginx:latest`, `docker image ls`, `docker tag`, `docker push`, `docker rmi` v�o file `docker-commands.md`.

6.  **C�c c�u l?nh v?i Docker Container:**
    * ?� ch?y v� ghi l?i output c?a c�c l?nh li�n quan ??n container (`docker run`, `docker ps`, `docker ps -a`, `docker exec`, `docker stop`, `docker start`, `docker rm`) v�o file `docker-container-commands.md`.

7.  **S? d?ng Docker image v� Docker Compose t?o m�i tr??ng ch?y ?ng d?ng PHP:**
    * ?� t?o th? m?c `my-php-app` v� c?u tr�c th? m?c b�n trong (`app`, `docker/nginx/conf`, `docker/php`, `docker/mysql`).
    * ?� t?o file `index.php` ??n gi?n.
    * ?� t?o c�c file `Dockerfile` cho Nginx, PHP, MySQL.
    * ?� t?o file `default.conf` cho Nginx.
    * ?� t?o file `docker-compose.yml` ?? ??nh ngh?a c�c service.
    * ?� th? kh?i ch?y m�i tr??ng PHP b?ng `docker-compose up -d --build`

8.  **Thay ??i c?u h�nh Docker Compose:**
    * ?� ch?nh s?a file `docker-compose.yml` trong th? m?c `my-php-app` ?? thay ??i t�n v� port c?a c�c service.
    * ?� ch?y l?i `docker-compose up -d --force-recreate --build` ?? �p d?ng thay ??i
    * ?� t?o file `docker-compose-config.md` v� ghi l?i c�c thay ??i trong `docker-compose.yml`.

9.  **S? d?ng Laradock t?o m�i tr??ng ch?y Laravel:**
    * ?� t?o th? m?c `Laradock` trong `E:/Deha-Academy-Docker-Lap1`.
    * ?� clone repository Laradock v�o th? m?c `Laradock`.
    * ?� sao ch�p v� ch?nh s?a file `.env` c?a Laradock ?? c?u h�nh `PHP_VERSION`, `NGINX_HOST_HTTP_PORT`, `MYSQL_VERSION`, v� `APP_CODE_PATH_HOST`.
    * ?� t?o th? m?c `laravel` ngang h�ng v?i th? m?c `Laradock`.
    * **Tr?ng th�i kh?i ch?y Laradock:** [Ch?y l?nh `docker compose up -d nginx php-fpm` ch?a th�nh c�ng do dung l??ng ? C m�y t�nh kh�ng ??, ?� c�i ??t l?i nhi?u l?n v�o ? E nh?ng Docker Desktop t? nh? c?u h�nh v�o ? C].

## C�c file ?� t?o:

* `docker-commands.md`
* `docker-container-commands.md`
* `my-php-app/` (v� c�c file b�n trong)
* `my-php-app/docker-compose.yml`
* `my-php-app/docker-compose-config.md`
* `Laradock/` (v� c�c file b�n trong)
* `Laradock/.env`
* `laravel/` 

## C�c thay ??i trong file `.env` c?a Laradock:
PHP_VERSION=8.1
 NGINX_HOST_HTTP_PORT=8000
 MYSQL_VERSION=5.7
 APP_CODE_PATH_HOST=../laravel/

