---
layout: post
title: 在Linux上安装字体
---

压缩windows字体

```shell
cd C:\WINDOWS\Fonts
tar czvf ttfs.tar.gz *.ttf

scp ttfs.tar.gz <remote machine>
```

安装

```shell
cd /usr/share/fonts
sudo mkdir all

cp <path of fonts> /usr/share/fonts/all

fc-cache -fv
```


验证

```shell
fc-match Arial -s
```