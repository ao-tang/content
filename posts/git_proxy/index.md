---
title: Git 代理设置方法
date: 2023-11-10T10:04:10Z
author: Tang Ao
tags:
  - git
draft: false
---
使用 `git clone` 仓库时网络影响还不大，但是用 `git submodule update --init --recursive` 或者 `git submodule update --remote` 更新子模块时常常卡得 p 爆。

## 1.全局代理

```
git config --global http.proxy http://127.0.0.1:7890
git config --global https.proxy https://127.0.0.1:7890
```

## 2.只对 GitHub 代理

```
git config --global http.https://github.com.proxy https://127.0.0.1:7890
git config --global https.https://github.com.proxy https://127.0.0.1:7890
```

是对https协议进行代理设置

## 3.取消

```
git config --global --unset http.proxy
git config --global --unset https.proxy
```

## 4.查看

```
git config --global -l
```
