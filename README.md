# Docker 정리

### new knowledge

- docker login 시 이메일이 아닌 username으로 로그인 하자.
- `-v` folder mount
- `-d` run background
- `-p` port binding
- `--name` set name
- `docker build` 로 imgae를 만들고 `run`으로 실행하자
- docker file 에서 `daemon off;` 로 지정해야 foreground로 웹서버가 돌아서 컨테이너 생성시 웹서버가 돌아간다.
- docker-compose 의 --volume=현재경로 : 컨테이너 경로로 마운트 (공유폴더)
- docker system prune -a -f 안쓰는 이미지 모두 지우기 (디스크 용량이 꽉찼어서 사용)