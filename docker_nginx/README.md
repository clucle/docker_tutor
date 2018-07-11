# Docker nginx

### steps

```bash
docker login
docker pull nginx:latest
docker run -d -p 80:80 --name nginx-container nginx
```

### new knowledge

- docker login 시 이메일이 아닌 username으로 로그인 하자.