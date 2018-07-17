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

- nginx 의 `-g` flag는 debugging symbols() 를 포함한다고한다.
- nginx 기본 static file path : `/usr/share/nginx/html`
- nginx 기본 conf file : `/etc/nginx/nginx.conf`

