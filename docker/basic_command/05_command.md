# exit

도커 컨테이너 내부로 들어갔는데 빠져나오고 싶을 때

```
【ctrl + p】 누르고 【ctrl + q】 누르면 빠져나온다.
```

일반

```
【ctrl + z】
【ctrl + c】
```

# 도커 컨테이너 명령어

### 동작중인 컨테이너 확인

```bash
$ docker ps
```

### 정지된 컨테이너 확인

```bash
$ docker ps -a
```

### 컨테이너 중지하기

```bash
$ docker stop [container id or name]
```

### 컨테이너 삭제하기

```bash
$ docker rm [container id or name]
```

### 삭제된 컨테이너 확인

```bash
$ docker ps -a
```

### 복수개의 컨테이너 삭제

```bash
$ docker rm [container id or name], [container id or name]
```

### 컨테이너 한번에 삭제

```bash
$ docker rm -f $(docker ps -a -q)
```

### 컨테이너를 삭제하기 전에 이미지를 삭제할 경우

-f 옵션을 붙이면 컨테이너도 강제삭제 된다.

```bash
$ docker rmi -f [image ID]
```

# 도커 이미지 명령어

### 현재 이미지 확인

```bash
$ docker images
```

### 이미지 삭제

```bash
$ docker rmi [image ID]
```

### 이미지 한번에 삭제

```bash
$ docker rmi $(docker images -q)
```

# 컨테이너 재부팅하기

```bash
$ docker restart [container id or name]
```
