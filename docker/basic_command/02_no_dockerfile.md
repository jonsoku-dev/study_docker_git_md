# image

docker hub 에서 ubnutu image 다운받기 (예제)

```bash
$ docker pull ubuntu:10.15-alpine
```

> ubuntu:10.15-alpine 부분이 자신이 원하는 이미지명

<hr/>

# Run

container로 image 실행하기

```bash
$ docker run -d ubuntu
```

- ubuntu : image name
- -d : 데몬 모드 (이거 안쓰면 해당 터미널탭 사용못하니까 귀찮음..)

<hr/>

## option

| 옵션   | 설명                                                        | 사용예제                               |
| ------ | ----------------------------------------------------------- | -------------------------------------- |
| -d     | 보통 데몬 모드라고 부르며 컨테이너가 백그라운드로 실행된다. | -d                                     |
| -p     | 호스트와 컨테이너의 포트를 연결                             | -p 3000:3000                           |
| -v     | 호스트와 컨테이너의 디렉토리를 연결 (마운트)                | -v ./client/:/app /app/node_modules    |
| -e     | 컨테이너 내에서 사용할 환경변수 설정                        | -e MYSQL_ROOT_PASSWORD=examplepassword |
| –-name | 컨테이너 이름 설정                                          | --name jonsoku                         |
| -–rm   | 프로세스 종료시 컨테이너 자동 제거                          | --rm                                   |
| -it    | -i와 -t를 동시에 사용한 것으로 터미널 입력을 위한 옵션      | -it                                    |
| –-link | 컨테이너 연결 [컨테이너명:별칭]                             | --link=”db:db”                         |

<hr/>
