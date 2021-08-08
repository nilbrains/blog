---
title: 【Debian】nvm管理多版本Node.js
categories:
  - 学习
tags:
  - node
abbrlink: 1490f60b
date: 2021-08-08 15:26:27
---

`nvm` 是一个管理`Node.js`版本的工具.

<!-- more -->

## 安装 nvm

```bash
git clone https://github.com/creationix/nvm.git ~/.nvm
cd ~/.nvm
git checkout `git describe --abbrev=0 --tags`
# 激活
. ~/.nvm/nvm.sh
```

在`~/.bashrc`加入

```bash
# 类似于 环境变量
export NVM_DIR=~/.nvm
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh"
[ -r $NVM_DIR/bash_completion ] && . $NVM_DIR/bash_completion
# 阿里云镜像
export NVM_NODEJS_ORG_MIRROR=https://npm.taobao.org/mirrors/node
```

## 常用nvm命令

### 显示所有可用版本

```bash
nvm ls-remote
```

### 安装最新长期版本

```bash
nvm install --lts
# or 
nvm install <version>
```

### 卸载

```bash
nvm uninstall <version>
```

### 使用指定版本

```bash
nvm use <version>
```

### 其它

#### 1. 还原环境变量PATH

```bash
nvm deactivate
```

#### 2. 迁移npm至新版本的Node.js

```bash
nvm install < new version > --reinstall-packages-from=< old version >
