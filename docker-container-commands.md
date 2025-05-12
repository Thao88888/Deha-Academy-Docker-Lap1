# Kết quả lệnh docker run -d --name my-nginx-test -p 8081:80 nginx:latest
  Admin@Admin MINGW64 /E/Deha-Academy-Docker-Lap1
$ docker run -d --name my-nginx-test -p 8081:80 nginx:latest
d21c2aa4772cf89db50d01df9b556101a698f13352f8c6cfa8192da5b9a951c6

# Kết quả lệnh docker ps
Admin@Admin MINGW64 /E/Deha-Academy-Docker-Lap1
$ docker ps
CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS
        PORTS                  NAMES
d21c2aa4772c   nginx:latest   "/docker-entrypoint.…"   39 seconds ago   Up 37 se
conds   0.0.0.0:8081->80/tcp   my-nginx-test


# Kết quả lệnh docker ps -a
Admin@Admin MINGW64 /E/Deha-Academy-Docker-Lap1
$ docker ps -a
CONTAINER ID   IMAGE          COMMAND                  CREATED              STAT
US              PORTS                  NAMES
d21c2aa4772c   nginx:latest   "/docker-entrypoint.…"   About a minute ago   Up A
bout a minute   0.0.0.0:8081->80/tcp   my-nginx-test

# Kết quả lệnh docker exec -it my-nginx-test bash
Admin@Admin MINGW64 /E/Deha-Academy-Docker-Lap1
$ docker exec -it my-nginx-test bash
root@d21c2aa4772c:/# 

# Kết quả lệnh ls -l bên trong container my-nginx-test
root@d21c2aa4772c:/# ls -l
total 64
lrwxrwxrwx   1 root root    7 Apr 28 00:00 bin -> usr/bin
drwxr-xr-x   2 root root 4096 Mar  7 17:30 boot
drwxr-xr-x   5 root root  340 May 11 15:39 dev
drwxr-xr-x   1 root root 4096 Apr 28 21:43 docker-entrypoint.d
-rwxr-xr-x   1 root root 1620 Apr 28 21:42 docker-entrypoint.sh
drwxr-xr-x   1 root root 4096 May 11 15:39 etc
drwxr-xr-x   2 root root 4096 Mar  7 17:30 home
lrwxrwxrwx   1 root root    7 Apr 28 00:00 lib -> usr/lib
lrwxrwxrwx   1 root root    9 Apr 28 00:00 lib64 -> usr/lib64
drwxr-xr-x   2 root root 4096 Apr 28 00:00 media
drwxr-xr-x   2 root root 4096 Apr 28 00:00 mnt
drwxr-xr-x   2 root root 4096 Apr 28 00:00 opt
dr-xr-xr-x 234 root root    0 May 11 15:39 proc
drwx------   2 root root 4096 Apr 28 00:00 root
drwxr-xr-x   1 root root 4096 May 11 15:39 run
lrwxrwxrwx   1 root root    8 Apr 28 00:00 sbin -> usr/sbin
drwxr-xr-x   2 root root 4096 Apr 28 00:00 srv
dr-xr-xr-x  11 root root    0 May 11 15:39 sys
drwxrwxrwt   2 root root 4096 Apr 28 00:00 tmp
drwxr-xr-x   1 root root 4096 Apr 28 00:00 usr
drwxr-xr-x   1 root root 4096 Apr 28 00:00 var

# Thoát khỏi shell của container bằng lệnh exit.
root@d21c2aa4772c:/# exit
exit

# Kết quả lệnh docker exec my-nginx-test nginx -v
Admin@Admin MINGW64 /E/Deha-Academy-Docker-Lap1
$ docker exec my-nginx-test nginx -v
nginx version: nginx/1.27.5

# Kết quả lệnh docker stop my-nginx-test
Admin@Admin MINGW64 /E/Deha-Academy-Docker-Lap1
$ docker stop my-nginx-test
my-nginx-test

# Kết quả lệnh docker start my-nginx-test
Admin@Admin MINGW64 /E/Deha-Academy-Docker-Lap1
$ docker start my-nginx-test
my-nginx-test


# Kết quả lệnh docker rm my-nginx-test
Admin@Admin MINGW64 /E/Deha-Academy-Docker-Lap1
$ docker stop my-nginx-test
my-nginx-test
Admin@Admin MINGW64 /E/Deha-Academy-Docker-Lap1
$ docker rm my-nginx-test
my-nginx-test

