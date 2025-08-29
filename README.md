## 目录
- [目录](#目录)
- [免责声明](#免责声明)
  - [1. 镜像容器适配](#1-镜像容器适配)
  - [2. 法律遵守](#2-法律遵守)
  - [3. 免责声明接受](#3-免责声明接受)
- [1. 简介](#1-简介)
- [2. 使用方式](#2-使用方式)
    - [2.1 使用 git 命令获取应用](#21-使用-git-命令获取应用)
    - [2.2 使用压缩包方式获取应用](#22-使用压缩包方式获取应用)
- [3. 备注](#3-备注)


***

## 免责声明

### 1. 镜像容器适配
本项目仅针对原`docker`镜像容器运行进行针对`1Panel`应用商店的适配。我们不对任何原始镜像的有效性做出任何明示或暗示的保证或声明，并且不对使用本仓库应用所造成的任何影响负责。用户在使用本项目时应自行承担风险。

### 2. 法律遵守
用户在使用本仓库时必须遵守所在国家与地区的法律法规。某些应用可能受到特定国家法律的限制，用户需自行了解并遵守相关法律要求。本仓库不对用户违反法律法规所产生的任何后果负责。

### 3. 免责声明接受
用户在导入本仓库并使用其中的应用时，即表示用户已经阅读、理解并同意接受本免责声明的所有条款和条件。

请注意，本免责声明仅针对本仓库的使用情况，并不包括其他第三方应用或服务。对于与本仓库链接的第三方内容，我们不对其准确性、完整性、可靠性或合法性负责。

在使用本仓库之前，请确保已经阅读、理解并接受了本免责声明的所有条款和条件。

***
## 1. 简介
这是一些适配`1Panel`商店`2.0`版本的docker应用配置。

致力于一键运行各种 Docker 应用。无需复杂配置，享受便利和高效。


## 2. 使用方式

### 2.1 使用 git 命令获取应用

`1Panel`计划任务类型`Shell 脚本`的计划任务框里，添加并执行以下命令，或者终端运行以下命令，
```shell
git clone -b main https://github.com/sephiroth233/appstore /opt/1panel/resource/apps/local/appstore-localApps

cp -rf /opt/1panel/resource/apps/local/appstore-localApps/apps/* /opt/1panel/resource/apps/local/

rm -rf /opt/1panel/resource/apps/local/appstore-localApps
```

然后应用商店刷新本地应用即可。

### 2.2 使用压缩包方式获取应用

`1Panel`计划任务类型`Shell 脚本`的计划任务框里，添加并执行以下命令，或者终端运行以下命令，
```shell
wget -P /opt/1panel/resource/apps/local https://github.com/sephiroth233/appstore/archive/refs/heads/main.zip

unzip -o -d /opt/1panel/resource/apps/local/ /opt/1panel/resource/apps/local/localApps.zip

cp -rf /opt/1panel/resource/apps/local/appstore-localApps/apps/* /opt/1panel/resource/apps/local/

rm -rf /opt/1panel/resource/apps/local/appstore-localApps

rm -rf /opt/1panel/resource/apps/local/localApps.zip
```

然后应用商店刷新本地应用即可。


## 3. 备注


**但是支持直接终端运行。**

> 本仓库应用基本支持直接 `docker-compose up` 运行

以`rustdesk`为例

```shell
# 进入 rustdesk 的最新版本目录
cd /opt/1panel/resource/apps/local/rustdesk/versions/latest/

# 复制 .env.sample 为 .env
cp .env.sample .env

# 编辑 .env 文件，修改参数
nano .env

# 启动 RustDesk
docker-compose up -d

# 查看连接所需密钥
cat ./data/hbbs/id_ed25519.pub

```

