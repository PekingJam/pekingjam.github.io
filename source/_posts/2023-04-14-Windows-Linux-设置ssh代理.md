---
title: Windows/Linux 设置ssh代理
top_img: 'linear-gradient(#e9619b, 15%, #fbd1e3);'
categories:
  - Windows
tags:
  - Linux
  - ssh
  - 代理
date: 2023-04-14 09:19:05
---

#### 设置方法
1. 编辑home目录下的`.ssh/config`文件
2. 在最后加入以下内容
```bash
	Host *
    Compression yes
    ServerAliveInterval 20
    ProxyCommand nc -X 5 -x 127.0.0.1:7890 %h %p
```
3. windwos则是以下配置

```bash

    Host *
    Compression yes
    ServerAliveInterval 20
    ProxyCommand "C:\Program Files\Git\mingw64\bin\connect.exe" -S 127.0.0.1:7890 %h %p
```
* `-X 5`表示socks5代理
