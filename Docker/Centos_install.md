```bash
docker pull centos:centos7
docker images

docker run -it -d --name centos1 centos:centos7

# it: ターミナルでコンテナを実行
# d: デーモンの略でバックグラウンドでコンテナを実行
# name: コンテナに名前をつける

docker ps

docker exec -it mycentos /bin/bash

# stop
docker stop centos1
docker ps

# start
docker start centos1

# net-tools install
yum install net-tools
```
