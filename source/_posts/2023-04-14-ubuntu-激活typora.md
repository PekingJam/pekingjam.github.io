---
title: ubuntu 激活typora
top_img: 'linear-gradient(#e9619b, 15%, #fbd1e3);'
categories:
  - Linux
tags:
  - typora
  - ubuntu
date: 2023-04-14 09:09:02
---
#### 效果图

![image-20230105212144543](https://oss.dandaner.cn/pd/publicshare/blog/image-20230105212144543.png)

#### 先决条件

1. 清醒且爱思考的大脑
2. 已安装官方typora软件的ubuntu系统
3. 流畅且无限制的网路环境

#### 编译环境搭建

1. 无需root权限，执行下面命令

   ```bash
   curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
   ```

2. 在弹出界面中输入 1 即可自动安装rust环境

3. 用以下命令校验是否安装成功

   ```bash
   ❯ rustc --version  
   rustc 1.66.0 (69f9c33d7 2022-12-12)
   
   ❯ cargo --version
   cargo 1.66.0 (d65d197ad 2022-11-15)
   ```

   

#### 编译

1. 克隆以下两个项目

   ```bash
   git clone https://github.com/DiamondHunters/NodeInject.git
   git clone https://github.com/DiamondHunters/NodeInject_Hook_example.git
   ```

2. 将`NodeInject_hooke_example`项目中hook.js 复制到 `NodeInject`项目中并替换`hooklog.js`

   ```bash
   cp NodeInject_Hook_example/hook.js ./NodeInject/src
   mv hook.js hooklog.js
   ```

3. 进入NodeInject目录并编译项目

   ```bash
   cd NodeInject
   cargo build
   ```

4. 将编译出的可执行文件复制到typora安装目录中并运行

   ```bash
   sudo cp ./target/debug/node_inject /usr/share/typora
   cd /usr/share/typora
   sudo ./node_inject
   ```
   * 输出以下结果为成功
      ```bash
      ❯ sudo ./node_inject
		extracting node_modules.asar
		adding hook.js
		applying patch
		packing node_modules.asar
		done!
		```

     

5. 进入`NodeInject_hooke_example`项目`license-gen`目录中编译软件

   ```bash
   cd NodeInject_hooke_example/license-gen
   cargo build
   ```

6. 运行以下命令生成激活秘钥

   ```bash
   ./target/debug/license-gen
   ```

7. 启动typora输入激活秘钥、邮箱任意填写即可。大功告成，尽情享用吧。

#### 笔者环境
* ubuntu 22.04
* typora 1.4.7

#### 鸣谢
*  DiamondHunters 提供的思路以及实现代码