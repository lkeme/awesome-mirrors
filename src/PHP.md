## 简介

Composer 安装时候会向国外的 Packagist 服务器发送请求，因为众所周知的原因，国内请求国外服务器，有时会出现不稳定甚至不可用的情况。  

镜像加速就是把国外的数据缓存到国内的服务器上，Composer 客户端只需配置服务器为国内的服务器，即可从国内服务器上下载，稳定性会有很高的提升。  

## 使用教程

```bash
# 全局配置
composer config -g repo.packagist composer https://mirrors.aliyun.com/composer/
# 取消全局配置
composer config -g --unset repos.packagist
```

```bash
# 项目配置
composer config repo.packagist composer https://mirrors.aliyun.com/composer/
# 取消项目配置
composer config --unset repos.packagist
```

```bash
# composer.json里面配置
{
    "repositories": {
        "packagist": {
          "description": "阿里云镜像",
            "type": "composer",
            "url": "https://mirrors.aliyun.com/composer/",
            "canonical": false
        }
    }
}
```

## 镜像列表

| 序号 | 网站                                           | 标签 | 时间         | 备注           |
|----|----------------------------------------------|----|------------|--------------|
| 1  | https://mirrors.aliyun.com/composer/         | 😊 | 2023-07-17 | 阿里云          |
| 2  | https://mirrors.cloud.tencent.com/composer/  | 😊 | 2023-07-17 | 腾讯云          |
| 3  | https://packagist.phpcomposer.com            | 😊 | 2023-07-17 | Composer 中文网 |
| 4  | https://packagist.mirrors.sjtug.sjtu.edu.cn  | 😊 | 2023-07-17 | 交通大学         |
| 5  | https://repo.huaweicloud.com/repository/php/ | 😫 | 2023-07-17 | 华为云          |

## 推荐相关项目

- [CRM - Composer 源管理工具](https://github.com/slince/composer-registry-manager)