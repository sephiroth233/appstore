[中文](https://github.com/okxlin/appstore/blob/localApps/README.md) | English
***

## Contribution Link

[**Click here to contribute with AFDIAN**](https://afdian.com/a/dockerapps)

[![**Click here to contribute with AFDIAN**](https://github.com/okxlin/appstore/raw/localApps/docs/afdian-logo.png)](https://afdian.com/a/dockerapps)

* * *

## Table of Contents

- [Contribution Link](#contribution-link)
- [Table of Contents](#table-of-contents)
- [Disclaimer](#disclaimer)
  - [1. Image Container Adaptation](#1-image-container-adaptation)
  - [2. Compliance with Laws](#2-compliance-with-laws)
  - [3. Acceptance of Disclaimer](#3-acceptance-of-disclaimer)
- [1. Introduction](#1-introduction)
  - [1Panel Third-Party App Store Categories and Introduction](#1panel-third-party-app-store-categories-and-introduction)
- [2. Usage](#2-usage)
  - [2.1 Domestic Network](#21-domestic-network)
    - [2.1.1 Getting Apps via Git Command](#211-getting-apps-via-git-command)
    - [2.1.2 Getting Apps via Compressed Package](#212-getting-apps-via-compressed-package)
  - [2.2 International Network](#22-international-network)
    - [2.2.1 Getting Apps via Git Command](#221-getting-apps-via-git-command)
    - [2.2.2 Getting Apps via Compressed Package](#222-getting-apps-via-compressed-package)
- [3. Remarks](#3-remarks)
- [4. App Overview](#4-app-overview)


***

## Disclaimer

### 1. Image Container Adaptation
This project specifically adapts to the `1Panel` app store for original `docker` image container operations. We do not make any explicit or implicit warranties or statements regarding the validity of any original images, and we are not responsible for any effects caused by using applications from this repository. Users undertake the risks associated with using this project on their own.

### 2. Compliance with Laws
When using this repository, users must comply with the laws and regulations of their respective countries and regions. Certain applications may be restricted by specific national laws, and users need to understand and comply with relevant legal requirements. This repository is not responsible for any consequences arising from the user's violation of laws and regulations.

### 3. Acceptance of Disclaimer
By importing and using the applications in this repository, the user signifies that they have read, understood, and accepted all the terms and conditions of this disclaimer.

Please note that this disclaimer applies only to the use of this repository and does not encompass other third-party applications or services. We are not responsible for the accuracy, completeness, reliability, or legality of third-party content linked to this repository.

Before using this repository, please ensure that you have read, understood, and accepted all the terms and conditions of this disclaimer.

***
## 1. Introduction
These are some configurations of docker applications adapted for the `1Panel` store version 2.0.

Dedicated to running various Docker applications with just one click. Enjoy convenience and efficiency without complex configurations.

### 1Panel Third-Party App Store Categories and Introduction

- https://1p.131.gs

**Special thanks to the author [@baozishu](https://github.com/baozishu)**

## 2. Usage

The default installation path of `1Panel` is `/opt/`, which can be modified as needed.

### 2.1 Domestic Network

> GitHub Acceleration Methods
>> - (Added to this repository) Self-built: https://github.com/hunshcn/gh-proxy
>> - https://ghp.ci

#### 2.1.1 Getting Apps via Git Command

In the `Shell Script` task type in the `1Panel` scheduled tasks, add and execute the following command, or run the following command in the terminal:

```shell
git clone -b localApps https://ghp.ci/https://github.com/okxlin/appstore /opt/1panel/resource/apps/local/appstore-localApps

cp -rf /opt/1panel/resource/apps/local/appstore-localApps/apps/* /opt/1panel/resource/apps/local/

rm -rf /opt/1panel/resource/apps/local/appstore-localApps
```

Then refresh the local applications in the app store.

#### 2.1.2 Getting Apps via Compressed Package

In the `Shell Script` task type in the `1Panel` scheduled tasks, add and execute the following command, or run the following command in the terminal:

```shell
wget -P /opt/1panel/resource/apps/local https://ghp.ci/https://github.com/okxlin/appstore/archive/refs/heads/localApps.zip

unzip -o -d /opt/1panel/resource/apps/local/ /opt/1panel/resource/apps/local/localApps.zip

cp -rf /opt/1panel/resource/apps/local/appstore-localApps/apps/* /opt/1panel/resource/apps/local/

rm -rf /opt/1panel/resource/apps/local/appstore-localApps

rm -rf /opt/1panel/resource/apps/local/localApps.zip
```

Then refresh the local applications in the app store.

### 2.2 International Network

#### 2.2.1 Getting Apps via Git Command

In the `Shell Script` task type in the `1Panel` scheduled tasks, add and execute the following command, or run the following command in the terminal:

```shell
git clone -b localApps https://github.com/okxlin/appstore /opt/1panel/resource/apps/local/appstore-localApps

cp -rf /opt/1panel/resource/apps/local/appstore-localApps/apps/* /opt/1panel/resource/apps/local/

rm -rf /opt/1panel/resource/apps/local/appstore-localApps
```

Then refresh the local applications in the app store.

#### 2.2.2 Getting Apps via Compressed Package

In the `Shell Script` task type in the `1Panel` scheduled tasks, add and execute the following command, or run the following command in the terminal:

```shell
wget -P /opt/1panel/resource/apps/local https://github.com/okxlin/appstore/archive/refs/heads/localApps.zip

unzip -o -d /opt/1panel/resource/apps/local/ /opt/1panel/resource/apps/local/localApps.zip

cp -rf /opt/1panel/resource/apps/local/appstore-localApps/apps/* /opt/1panel/resource/apps/local/

rm -rf /opt/1panel/resource/apps/local/appstore-localApps

rm -rf /opt/1panel/resource/apps/local/localApps.zip
```

Then refresh the local applications in the app store.

## 3. Remarks

**If an application is not displayed in the local app list, it means it has not been fully adapted for operation in the app store panel.**

**However, it can still be run directly in the terminal.**

> Most applications in this repository support running directly with `docker-compose up`

Taking `rustdesk` as an example:

```shell
# Enter the latest version directory of rustdesk
cd /opt/1panel/resource/apps/local/rustdesk/versions/latest/

# Copy .env.sample as .env
cp .env.sample .env

# Edit the .env file and modify the parameters
nano .env

# Start RustDesk
docker-compose up -d

# View the necessary key for connecting
cat ./data/hbbs/id_ed25519.pub

```

## 4. App Overview

![](https://github.com/okxlin/appstore/raw/localApps/docs/app-list.png)
