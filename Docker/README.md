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
- `--volume [VOLUME NAME]:[PATH]` or `-v` : 볼룸 연결
- `--mount type=bind,source=[PATH],target=[PATH],[OPTION]` : 로컬 디렉토리와 컨테이너를 연결하여 양방향 동작 수행
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
`--force` or `-f` : 실행 중인 컨테이너라도 명령 실행
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

### Docker Image 등록

```md
`docker image push [DOCKER ID]/[IMAGE NAME]` : 도커 이미지 도커 허브에 등록
```

### Docker Image 정보

```md
`docker image history [IMAGE NAME]` : 이미지의 모든 레이어의 정보 출력
```

### Docker Network 생성

```md
`docker network create [NAME] : 컨테이너 간 통신이 가능한 도커 네트워크 생성
```

### Docker File

```md
`FROM [IMAGE] AS [NAME]` : 이미지의 시작 이미지 설정
`ENV` : 환경 변수 값 지정 [key]=["value"]
`WORKDIR` : 디렉토리를 만들고 작업 디렉토리 지정
`COPY` : 로컬 파일을 복사 [원본경로] [복사경로]

- `--from=[STAGE NAME] [SOURCE PATH] [DESTINATION PATH]` : 해당 빌드 단계의 파일 복사
  `CMD` : 이미지를 컨테이너로 실행 시 실행할 명령 지정
  `RUN` : 컨테이너 안에서 명령 실행 후 결과를 이미지 레이어에 저장
  `EXPORT [PORT]` : 컨테이너가 외부에 접속할 포트 설정
  `VOLUME [PATH]` : 볼룸 설정
```
