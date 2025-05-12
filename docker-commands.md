# Kết quả lệnh docker login
Admin@Admin MINGW64 /E/Deha-Academy-Docker-Lap1
$ docker login
Authenticating with existing credentials... [Username: thuthao88]

i Info → To login with a different account, run 'docker logout' followed by 'doc
ker login'


Login did not succeed, error: error during connect: in the default daemon config
uration on Windows, the docker client must be run with elevated privileges to co
nnect: Post "http://%2F%2F.%2Fpipe%2Fdocker_engine/v1.48/auth": open //./pipe/do
cker_engine: The system cannot find the file specified.

USING WEB-BASED LOGIN

i Info → To sign in with credentials on the command line, use 'docker login -u <
username>'


Your one-time device confirmation code is: KMZR-RRCH
Press ENTER to open your browser or submit your device code here: https://login.
docker.com/activate

Waiting for authentication in the browser…
Login Succeeded

# Kết quả lệnh docker logout
Admin@Admin MINGW64 /E/Deha-Academy-Docker-Lap1
$ docker logout
Removing login credentials for https://index.docker.io/v1/

# Kết quả lệnh docker version
Admin@Admin MINGW64 /E/Deha-Academy-Docker-Lap1
$ docker version
Client:
 Version:           28.0.4
 API version:       1.48
 Go version:        go1.23.7
 Git commit:        b8034c0
 Built:             Tue Mar 25 15:07:48 2025
 OS/Arch:           windows/amd64
 Context:           default
error during connect: in the default daemon configuration on Windows, the docker
 client must be run with elevated privileges to connect: Get "http://%2F%2F.%2Fp
ipe%2Fdocker_engine/v1.48/version": open //./pipe/docker_engine: The system cann
ot find the file specified.

# Kết quả lệnh docker pull nginx:latest
Admin@Admin MINGW64 /E/Deha-Academy-Docker-Lap1
$ docker pull nginx:latest
latest: Pulling from library/nginx
d3dc5ec71e9d: Pull complete
913115292750: Pull complete
3e544d53ce49: Pull complete
d38f2ef2d6f2: Pull complete
254e724d7786: Pull complete
40a6e9f4e456: Pull complete
4f21ed9ac0c0: Pull complete
Digest: sha256:c15da6c91de8d2f436196f3a768483ad32c258ed4e1beb3d367a27ed67253e66
Status: Downloaded newer image for nginx:latest
docker.io/library/nginx:latest

# Kết quả lệnh docker image ls (trước khi tag và push)
Admin@Admin MINGW64 /E/Deha-Academy-Docker-Lap1
$ docker image ls
REPOSITORY   TAG       IMAGE ID       CREATED       SIZE
nginx        latest    c15da6c91de8   3 weeks ago   279MB

# Kết quả lệnh docker tag nginx:latest thuthao88/my-nginx:latest
Admin@Admin MINGW64 /E/Deha-Academy-Docker-Lap1
$ docker tag nginx:latest thuthao88/my-nginx:latest

# Kết quả lệnh docker push thuthao88/my-nginx:latest
Admin@Admin MINGW64 /E/Deha-Academy-Docker-Lap1
$ docker push thuthao88/my-nginx:latest
The push refers to repository [docker.io/thuthao88/my-nginx]
d38f2ef2d6f2: Mounted from library/nginx
4f21ed9ac0c0: Mounted from library/nginx
40a6e9f4e456: Mounted from library/nginx
d3dc5ec71e9d: Mounted from library/nginx
3e544d53ce49: Mounted from library/nginx
254e724d7786: Mounted from library/nginx
913115292750: Mounted from library/nginx
latest: digest: sha256:88b3388ea06c7262e410a3ab5c05dc4088b7b39dea569addd8c30766f
4f47440 size: 2292

i Info → Not all multiplatform-content is present and only the available single-
platform image was pushed
         sha256:c15da6c91de8d2f436196f3a768483ad32c258ed4e1beb3d367a27ed67253e66
 -> sha256:88b3388ea06c7262e410a3ab5c05dc4088b7b39dea569addd8c30766f4f47440


# Kết quả lệnh docker rmi thuthao88/my-nginx:latest
Admin@Admin MINGW64 /E/Deha-Academy-Docker-Lap1
$ docker rmi thuthao88/my-nginx:latest
Untagged: thuthao88/my-nginx:latest

# Kết quả lệnh docker image ls (sau khi xóa)
Admin@Admin MINGW64 /E/Deha-Academy-Docker-Lap1
$ docker image ls
REPOSITORY   TAG       IMAGE ID       CREATED       SIZE
nginx        latest    c15da6c91de8   3 weeks ago   279MB




