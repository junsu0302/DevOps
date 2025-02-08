# Docker Registry

1. 래지스트리 이미지로 도커 레지스트리 실행

```md
`docker container run -d -p [ROCAL PORT]:[CONTAINER PORT] --restart always [IMAGE NAME]`

- `--restart` : 도커를 재시작했을 때 해당 컨테이너도 자동 재실행
```

2. 로컬 컴퓨터에 레지스트리 별명 추가

```md
`echo $'\n127.0.0.1 [REGISTRY NAME]' | sudo tee -a /etc/hosts`
```

3. Docker의 daemon.json에 레지스트리 설정 추가(Docker Engine)

```md
`"insecure-registries" : ["[REGISTRY NAME]:[PORT]"]`
```

3. 이미지 첨부

```md
`docker image tag [IMAGE NAME] [REGISTRY NAME]:[PORT]/[PATH]:[VERSION]` : 레지스트리의 원하는 장소에 이미지 참조 부여
`docker image push [REGISTRY NAME]:[PORT]/[PATH]:[VERSION]` : 이미지 업로드
```
