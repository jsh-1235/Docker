# docker command

- docker -v
- docker pull httpd
- docker images
- docker ps
- docker ps -a
- docker run --name ws httpd
- docker stop ws
- docker start ws
- docker logs ws
- docker logs -f ws
- docker rm ws (docker stop ws)
- docker rm -f ws
- docker rm --force ws
- docker rmi httpd

## docker Host

- docker run --name ws -p 80:80 httpd
- docker container rename CONTAINER NEW_NAME

## docker Container

- docker container cli
- docker exec ws pwd
- docker exec -it ws /bin/sh
- docker exec -it ws /bin/bash
- exit
- apt update
- apt install nano

## 호스트와 컨테이너의 파일시스템 연결

- docker run --name [컨테이너이름] -p [Host포트번호]:80 -v [Host파일시스템]:[컨테이너파일시스템] httpd
- docker run --name ws -p 80:80 -v C:/Projects/Docker/web:/usr/local/apache2/htdocs/ httpd

## docker images

- docker build -f Dockerfile -t fun-docker .
- docker images
- docker run -d -p 8080:8080 fun-docker
- docker run --name ws -p 80:80 httpd
