---
layout: "post"
title: "useful commands"
date: "2017-04-28 16:16"
categories: technique
tags: [command]
keywords: command
toc:
---

### linux添加用户的相关命令
1. useradd  添加用户
`useradd -d /home/wengqiang -m wengqiang -s /bin/bash`
创建用户wengqiang

2. usermod 修改创建用户的相关属性
`usermod -s /bin/sh wengqiang`
修改用户wengqiang的登录shell

`usermod -aG sudo wengqiang`
将用户wengqinag加入到sudo group中

3. passwd 修改用户的密码
`passwd wengqiang`


### 修改文件的owner以及group
`chown owner_name:group_name file_name`

<!-- more -->


### linux|mac 产生随机串
1. linux上 `cat /dev/urandom | tr -dc A-Z9 | head -c ${1:-81}`
2. mac上 `cat /dev/urandom | LC_ALL=C tr -dc 'A-Z9' | fold -w 81 | head -n 1`


### windows下验证校验码命令
`Certutil`(Certutil /?)

```
certutil -hashfile xxx MD5
certutil -hashfile xxx SHA1
certutil -hashfile xxx SHA256
```

### 获取本机ip

`curl ip.cn`


### 使用openssl生成secp256k1的key-pair

1. 生成
`openssl ecparam -name secp256k1 -genkey -out ec-priv.pem`

2. 输出
`openssl ec -in ec-priv.pem -text -noout`
