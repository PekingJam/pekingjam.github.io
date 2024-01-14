---
title: Microsoft E5 调用API续订教程：Microsoft 365 E5 Renew X
top_img: 'linear-gradient(#e9619b, 15%, #fbd1e3);'
categories:
  - Linux
tags:
  - Microsoft 365
  - E5
  - 续订
date: 2024-01-14 16:42:18
---

#### 简介

Microsoft 365 E5 Renew X是一款网页版的E5续订服务，其依赖网页浏览器呈现支持用户多端操作，完全将E5账户API调用托管在了服务器端因此用户无需电脑也可使用。

### 使用教程

#### 1. 应用注册

1. 点击登录 Azure或点击直接进入Azure应用注册，登录账号使用申请到的Microsoft 365 E5的管理员账户（账户名类似XXXX@YYYY.onmicrosoft.com格式）。

2. 登录完成后点击右上角的“门户”按钮进入Azure管理中心，在搜索栏内输入“应用注册”，点击进入（若应用注册搜索不到请点击此处直接进入）。

   ![image-20240114180628915](https://cloud.dandaner.cn/p/publicshare/blog/image-20240114180628915.png)

3. 点击"新注册"按钮

   ![image-20240114180741808](https://cloud.dandaner.cn/p/publicshare/blog/image-20240114180741808.png)

4. 配置应用 应用名称随意写、注意可访问性选项选择最后一项、重定向URL暂时不填 、完成后点击注册

   ![image-20240114180923604](https://cloud.dandaner.cn/p/publicshare/blog/image-20240114180923604.png)

#### 2.配置应用重定向URL（身份验证）

1. 先点击“概述”，然后点击“添加重定向URL”，进入重定向URL配置界面，**下图中的应用程序(客户端)ID即为"客户端ID"**。

   ![image-20240114181044038](https://cloud.dandaner.cn/p/publicshare/blog/image-20240114181044038.png)

2. 点击“添加平台”，再点击“移动和桌面应用程序”，

   ![image-20240114181103403](https://cloud.dandaner.cn/p/publicshare/blog/image-20240114181103403.png)

3. 继续勾选中第一个URL，最后点击底部的“配置”，该URL为"https://login.microsoftonline.com/common/oauth2/nativeclient”也可手动添加"

   ![image-20240114181119904](https://cloud.dandaner.cn/p/publicshare/blog/image-20240114181119904.png)

4. 配置默认客户端类型将应用程序视为公共客户端 点击切换按钮为“是” ，最后点击“保存”按钮保存。

   ![image-20240114181429514](https://cloud.dandaner.cn/p/publicshare/blog/image-20240114181429514.png)


#### 3.配置应用程序的API权限

1. 登录调用必须权限图示

![image-20240114181611410](https://cloud.dandaner.cn/p/publicshare/blog/image-20240114181611410.png)

2. 手动配置权限

![image-20240114181649297](https://cloud.dandaner.cn/p/publicshare/blog/image-20240114181649297.png)

3. 选择"委托的权限"

![image-20240114181727345](https://cloud.dandaner.cn/p/publicshare/blog/image-20240114181727345.png)

4. 根据编辑页面中列出的API权限需求表（注意在程序中切换为"**登录**“）来勾选所对应的API权限，全部选择完成后点击"添加权限”。

![image-20240114181812407](https://cloud.dandaner.cn/p/publicshare/blog/image-20240114181812407.png)

5. 添加权限效果图,如果没有“代表XXX授予管理员同意”按钮 说明该账号不是管理员账号 换登管理员账号创建应用

   ![image-20240114181926542](https://cloud.dandaner.cn/p/publicshare/blog/image-20240114181926542.png)

#### 3. 在后台添加运行账号

![image-20240114182117516](https://cloud.dandaner.cn/p/publicshare/blog/image-20240114182117516.png)