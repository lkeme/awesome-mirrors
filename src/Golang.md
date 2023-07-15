## 简介

国内从 DockerHub 拉取镜像有时会遇到困难，此时可以配置镜像加速器。Docker 官方和国内很多云服务商都提供了国内加速器服务。

## 使用教程

```bash
# 配置镜像
sudo mkdir -p /etc/docker
sudo tee /etc/docker/daemon.json <<-'EOF'
{
    "registry-mirrors": [
        "https://example.test"
    ]
}
EOF
sudo systemctl daemon-reload
sudo systemctl restart docker

```

## 镜像列表

| 序号 | 网站                                       | 标签 | 时间         | 备注           |
|----|------------------------------------------|----|------------|--------------|
| 1  | https://hub-mirror.c.163.com/            | 😊 | 2023-07-15 | 网易云          |
| 2  | https://dockerproxy.com/                 | 😊 | 2023-07-15 | DockerProxy  |
| 3  | https://mirror.baidubce.com/             | 😊 | 2023-07-15 | 百度云          |
| 4  | https://docker.nju.edu.cn/               | 😊 | 2023-07-15 | 南京大学镜像站      |
| 5  | https://docker.mirrors.sjtug.sjtu.edu.cn | 😊 | 2023-07-15 | 上海交大镜像站      |
| 6  | https://docker.m.daocloud.io/            | 😊 | 2023-07-15 | DaoCloud 镜像站 |  

