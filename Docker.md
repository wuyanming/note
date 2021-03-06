### 查看docker信息
docker info

### 拉取一个镜像。名字是node,版本是4
docker pull node:4

### 查看本地镜像
docker images [name:tag]

### 删除镜像/容器
docker rm [name:id] 删除容器
docker rmi [id] 删除镜像

### 列出所有正在运行的镜像
docker ps
-a 列出当前系统中所有容器
-l 列出最后一次使用的容器

### 重新启动容器
docker start [name|id]

### 停止容器
docker stop [name|id]

### 附着到容器上
docker attach [name|id]

### 查看容器内进程
docker top [name|id]

### docker run [OPTIONS] IMAGE[:TAG] [COMMAND] [ARG...]
--name 容器名字
--restart=[always|on-failure:5] 自动重启
-d 后台运行
-v 共享文件系统
-i -t 进入交互式环境
--link 连接到另外一个容器。e.g, --link redis-name:redis_alias
--rm 运行完删除
-m 内存大小
-c cpu优先级和调度周期
-e 环境变量 e.g, -e "deep=purple"
-h hostname
-u 指定用户，默认root
-w 工作目录，默认/
-p 绑定端口 e.g, -p 50122:22 主机的50122端口映射到容器的22端口

### 获取容器信息
docker inspect [name:id]
-f | --format '{{ .key1.key1 }}' 类似获取json对象值的方式来获取值

### 查看端口绑定短息
docker port
