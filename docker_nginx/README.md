# Docker nginx


## run by command line

### run nginx steps

```bash
docker login
docker pull nginx:latest
docker run -d -p 80:80 --name nginx-container nginx
```

### enter in container

```bash
docker exec -it container-id /bin/bash
```

### clean

```bash
docker ps // before nginx clean
docker stop nginx-container
docker rm -f nginx-container
docker ps // after nginx clean
```

### imgae clean

```bash
docker images // before clean nginx imgae
docker rmi nginx
docker images // after clean nginx imgae
```

## build Dockerfile, run use my image

```bash
docker build -t docker_nginx_img(tag) .(dir)
docker run -d -p 80:80 --name my-nginx-container docker_nginx_img
```

### new knowledge

- docker login 시 이메일이 아닌 username으로 로그인 하자.
- `-v` folder mount
- `-d` run background
- `-p` port binding
- `--name` set name
- `docker build` 로 imgae를 만들고 `run`으로 실행하자
- docker file 에서 `daemon off;` 로 지정해야 foreground로 웹서버가 돌아서 컨테이너 생성시 웹서버가 돌아간다.
- nginx 의 `-g` flag는 debugging symbols() 를 포함한다고한다.
- nginx 기본 static file path : `/usr/share/nginx/html`
- nginx 기본 conf file : `/etc/nginx/nginx.conf`
