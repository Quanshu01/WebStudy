

# Docker查看IP地址

## 方法一：使用docker inspect命令

docker inspect命令可以查看Docker容器的详细信息，包括IP地址等。具体操作步骤如下：

1. 打开终端并登录到Docker主机。
2. 输入以下命令：`docker inspect <container_id> | grep IPAddress`（其中<container_id>为容器ID，可使用docker ps命令查看）。
3. 按下Enter键，就可以看到容器的IP地址。

值得注意的是，由于容器可能会有多个IP地址，因此在命令行查看IP地址时需要自己进行筛选。

## 方法二：使用Docker自带工具docker exec命令

docker exec命令可以在运行的Docker容器中执行命令，不仅可以帮助我们查看容器IP地址，还可以执行其他命令。具体操作步骤如下：

1. 打开终端并登录到Docker主机。
2. 输入以下命令：`docker exec <container_id> ifconfig`（其中<container_id>为容器ID，可使用docker ps命令查看）。
3. 按下Enter键，就可以查看到容器的IP地址。

需要注意的是，不同操作系统或发行版下的容器中，ifconfig命令的输出可能不一样。可以考虑使用ip addr命令作替代。