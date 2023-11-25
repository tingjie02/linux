# Linux Configuration Guide

This guide provides instructions for configuring your Linux system.

## Debian
To set up the package sources for Debian 12 "Bookworm", run the following command:
```bash
sudo wget -O /etc/apt/sources.list https://raw.githubusercontent.com/tingjie02/linux/main/debian-bookworm-sources.list
```

For Debian 11 "Bullseye", use this command:
```bash
sudo wget -O /etc/apt/sources.list https://raw.githubusercontent.com/tingjie02/linux/main/debian-bullseye-sources.list
```

For Debian 10 "Buster", execute this command:
```bash
sudo wget -O /etc/apt/sources.list https://raw.githubusercontent.com/tingjie02/linux/main/debian-buster-sources.list
```

&nbsp;
# Backports Repository
To enable the Backports Repository, which offers access to newer versions of packages, use the following command:
```bash
sudo sed -i 's/^# deb /deb /' /etc/apt/sources.list
```

&nbsp;
# 中国镜像站
要使用清华大学开源软件镜像站，请执行以下命令：
```bash
sudo sed -i 's#deb.debian.org#mirrors.tuna.tsinghua.edu.cn#' /etc/apt/sources.list
```
要使用网易开源软件镜像站，请执行以下命令：
```bash
sudo sed -i 's#deb.debian.org#mirrors.163.com#' /etc/apt/sources.list
```