###### Docker 快速删除所有容器

2017年11月08日 11:42:29

阅读数：3244

## 查看运行容器

```
docker ps1
```

## 查看所有容器

```
docker ps -a1
```

## 进入容器

其中字符串为容器ID:

```
docker exec -it d27bd3008ad9 /bin/bash1
```

## 1.停用全部运行中的容器:

```
docker stop $(docker ps -q)1
```

## 2.删除全部容器：

```
docker rm $(docker ps -aq)1
```

## 3.一条命令实现停用并删除容器：

```
docker stop $(docker ps -q) & docker rm $(docker ps -aq)
```