# Docker Volume

### Volume 생성

```md
`docker volume create [VOLUME NAME]` : 볼룸 생성
```

### Volume 정보 확인

```md
`docker volume ls` : 볼룸 정보 확인
`docker container inspect --format '{{.Mounts}}' [CONTAINER NAME]` : 해당 컨테이너의 볼륨 정보 확인
```
