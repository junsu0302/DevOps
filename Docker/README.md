# Docker

### Docker Container 실행

```md
`docker container run [OPTIONS] [IMAGE]` : 컨테이너로 애플리케이션 실행

- `--interactive` : 컨테이너에 접속
- `--tty` : 터미널을 통해 컨테이너 조작
- `--publish [HOST PORT:CONTAINER PORT]` : 호스트 PORT로 들어온 트래픽을 컨테이너 PORT로 전달
- `--detach` : 컨테이너를 백그라운드에서 실행
```

### Docker Container 정보 확인

```md
`docker container ls` : 실행 중인 컨테이너 정보 출력
`docker container ls --all` : 모든 컨테이너 정보 출력
`docker container logs [CONTAINER ID]` : 대상 컨테이너에서 수집된 모든 로그 출력
`docker container inspect [CONTAINER ID]` : 대상 컨테이너의 상세 정보 출력
`docker container stats` : 실행 중인 컨테이너 상태 확인
```

### Docker Container 삭제

```md
`docker container rm [OPTION] [CONTAINER ID]` : 컨테이너 삭제
`--force` : 실행 중인 컨테이너라도 삭제
CONTAINER ID에 $(docker container ls --all -q)입력 시 모든 컨테이너 삭제
```

### Docker Container 수정

```md
`docker container cp [LOCAL PATH] [CONTAINER ID]:[CONTAINER PATH]` : LOCAL PATH 내용을 CONTAINER PATH에 복사
`docker container exec [OPTION] [CONTAINER ID] [COMMAND] [COMMAND OPTION]` : 실행 중인 컨테이너에서 내부 명령 수행
```
