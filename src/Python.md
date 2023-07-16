## 简介

因国内网络问题，直接 pip 安装包有时速度会非常慢，而且经常会出现装到一半失败了的问题。  
既然这样，我们就要充分利用国内镜像的力量，节省时间，明显提高 pip 安装的效率。  

## 使用教程

```bash
# 临时使用
pip install -i https://pypi.doubanio.com/simple/ requests
# 永久使用
pip config set global.index-url https://pypi.doubanio.com/simple/
```

```conf
# 文件方式添加
[global]
index-url = https://pypi.doubanio.com/simple/
[install] 
trusted-host=pypi.douban.com
```

```bash
# 如果使用的是 http 的源，会报如下错误
# WARNING: Retrying (Retry(total=4, connect=None, read=None, redirect=None, status=None)) after connection broken by 'ProtocolError('Connection aborted.', RemoteDisconnected('Remote end closed connection without response'))': /simple/requests/
# 解决办法
pip install requests -i http://pypi.douban.com/simple --trusted-host pypi.douban.com
```

```bash
# 升级 pip
pip install -i https://pypi.doubanio.com/simple/ --upgrade pip 
```

## 镜像列表

| 序号 | 网站                                             | 标签 | 时间         | 备注              |
|----|------------------------------------------------|----|------------|-----------------|
| 1  | https://pypi.doubanio.com/simple/              | 😊 | 2023-07-16 | 豆瓣(https/http)  |
| 2  | https://mirrors.aliyun.com/pypi/simple/        | 😊 | 2023-07-16 | 阿里云(https/http) |
| 3  | https://pypi.tuna.tsinghua.edu.cn/simple/      | 😊 | 2023-07-16 | 清华大学            |
| 4  | https://mirrors.bfsu.edu.cn/pypi/web/simple/   | 😊 | 2023-07-16 | 北京外国语大学         |
| 5  | https://pypi.mirrors.ustc.edu.cn/simple/       | 😊 | 2023-07-16 | 中国科学技术大学        |
| 6  | https://mirrors.cloud.tencent.com/pypi/simple/ | 😊 | 2023-07-16 | 腾讯云(https/http) |
| 7  | https://pypi.org/simple/                       | 😊 | 2023-07-16 | 官方              |
