# Docker基本使用



## Ubuntu安装Docker

1. 安装docker

   `curl -sSL https://get.daocloud.io/docker | sh`

2. 安装docker-compose

   `sudo curl -L https://github.com/docker/compose/releases/download/1.16.1/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose`

tips:

错误1: ` /usr/local/bin/docker-compose: Permission denied`

解决1: `chmod +x /usr/local/bin/docker-compose`