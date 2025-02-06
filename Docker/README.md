# Docker

### Docker Container 실행

```md
`docker container run [OPTIONS] [IMAGE]` : 컨테이너로 애플리케이션 실행

- `--interactive` : 컨테이너에 접속
- `--tty` : 터미널을 통해 컨테이너 조작
- `--publish [HOST PORT:CONTAINER PORT]` : 호스트 PORT로 들어온 트래픽을 컨테이너 PORT로 전달
- `--detach` or `-d` : 컨테이너를 백그라운드에서 실행
- `--name` : 컨테이너 이름 설정
- `--env [KEY]:[VALUE] [IMAGE]` or `-e`: 컨테이너 환경 변수 설정
```

### Docker Container 정보

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
`--force` or `-f` : 실행 중인 컨테이너라도 삭제
CONTAINER ID에 $(docker container ls --all -q)입력 시 모든 컨테이너 삭제
```

### Docker Container 수정

```md
`docker container cp [LOCAL PATH] [CONTAINER ID]:[CONTAINER PATH]` : LOCAL PATH 내용을 CONTAINER PATH에 복사
`docker container exec [OPTION] [CONTAINER ID] [COMMAND] [COMMAND OPTION]` : 실행 중인 컨테이너에서 내부 명령 수행
```

### Docker Image 로드

```md
`docker image pull [IMAGE NAME]` : 해당 이미지 다운로드
```

### Docker Image 생성

```md
`docker image build [OPTION] [PATH]: dockerfile에 맞는 이미지 생성

- `--tag [NAME]` or `-t` : 이미지 이름 설정
```

### docker Image 정보

```md
`docker image history [IMAGE NAME]` : 이미지의 모든 레이어의 정보 출력
```

### Docker File

```md
`FROM` : 이미지의 시작 이미지 설정
`ENV` : 환경 변수 값 지정 [key]=["value"]
`WORKDIR` : 디렉토리를 만들고 작업 디렉토리 지정
`COPY` : 로컬 파일을 복사 [원본경로] [복사경로]
`CMD` : 이미지를 컨테이너로 실행 시 실행할 명령 지정
```
