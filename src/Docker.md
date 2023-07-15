## 简介

Go Module代理仓库服务，代理并缓存go模块。  你可以利用该代理来避免DNS污染导致的模块拉取缓慢或失败的问题，加速你的构建。

## 使用教程

```bash
# Bash
# Enable the go modules feature
export GO111MODULE=on
# Set the GOPROXY environment variable
export GOPROXY=https://gonexus.dev
``` 

```bash
# PowerShell
# Enable the go modules feature
$env:GO111MODULE=on
# Set the GOPROXY environment variable
$env:GOPROXY=https://gonexus.dev
```

```bash          
# Go >= 1.13
go env -w GOPROXY=https://gonexus.dev,direct
```

## 镜像列表

| 序号 | 网站                                | 标签 | 时间          | 备注      |
|------|-------------------------------------|------|---------------|-----------|
| 1    | https://proxy.golang.org/           | 😊 | 2023-07-15 | 官方      |
| 2    | https://goproxy.io/                 | 😊 | 2023-07-15 | GOPROXY   |
| 3    | https://mirrors.aliyun.com/goproxy/ | 😊 | 2023-07-15 | 阿里云    |
| 4    | https://proxy.golang.com.cn/        | 😊 | 2023-07-15 | GOPROXY   |
| 5    | https://goproxy.cn/                 | 😊 | 2023-07-15 | 七牛云    |
| 6    | https://gonexus.dev/                | 😊 | 2023-07-15 | Nexus社区 |
| 7    | http://goproxy.baidu.com/           | 😊 | 2023-07-15 | 百度      |
| 8    | https://athens.azurefd.net/         | 😊 | 2023-07-15 | Athens    |
