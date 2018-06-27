# TOUGHRADIUS

[![Build Status](https://travis-ci.org/talkincode/ToughRADIUS.svg?branch=master)](https://travis-ci.org/talkincode/ToughRADIUS)

## 开发和部署指南

由于依赖的软件较多，手动安装后，程序有些页面无法正常访问，怀疑是某些软件版本的问题，所以建议使用 docker 开发和部署程序。步骤如下：

### requirements

1. 安装docker: `yum install docker`

### 开发

1. 在 `tr-v2` 分支上进行开发，`commit` 后执行如下操作
2. 切换到 `build/dev` 目录， 构建镜像 `docker build . -t toughradius:latest`
3. 启动容器 `docker run -d -p 0.0.0.0:1815:1816 toughradius:latest`
4. 开放服务器的1816 端口，浏览器访问 `服务器ip:1815` 即可访问管理系统

## 上线

1. 将 `tr-v2` 分支的代码合并到 `release` 分支
2. 切换到 `build/dev` 目录， 构建镜像 `docker build . -t toughradius:release`
4. 启动容器 `docker run -d -p 0.0.0.0:1816:1816 toughradius:release`
5. 开放服务器的1816 端口，浏览器访问 `服务器ip:1816` 即可访问管理系统

## TOUGHRADIUS 简介

TOUGHRADIUS是一个开源的Radius服务软件，采用 Apache License 2.0 许可协议发布。

TOUGHRADIUS支持标准RADIUS协议，提供完整的AAA实现。支持灵活的策略管理，支持各种主流接入设备并轻松扩展，具备丰富的计费策略支持。

TOUGHRADIUS支持使用Oracle, MySQL, PostgreSQL, MSSQL等主流数据库存储用户数据，并支持数据缓存，极大的提高了性能。

TOUGHRADIUS支持Windows，Linux，BSD跨平台部署，部署使用简单。

TOUGHRADIUS提供了RADIUS核心服务引擎与Web管理控制台，以及可扩展的API。

TOUGHRADIUS网站：http://www.toughradius.net


## 功能特性

- 标准Radius认证记账支持，提供完整的AAA实现。
- 支持pap，chap，mschap-v2验证。
- 提供基于WEB的管理控制台界面。
- 提供基于WEB的自助服务系统，支持界面定制。
- 基于微信公众号的自助服务系统，支持微信在线支付。
- 基于Python Twisted高性能异步网络框架开发的认证计费引擎。
- Docker部署支持，支持Windows，Linux，BSD跨平台部署，部署使用简单。
- 支持各种主流接入设备(RouterOS,思科，华为，爱立信，中兴，阿尔卡特，H3C等)并轻松扩展，支持多设备接入管理。
- 支持使用Oracle, MySQL, PostgreSQL, MSSQL等主流数据库存储数据，并支持高速数据缓存。
- 支持预付费时长，预付费流量，预付费包月，买断包月，买断时长，买断流量资费策略。
- 支持最大会话时长定制。
- 支持数据库定时备份，定时删除过期备份，在线备份下载，导入恢复。
- 支持用户在线查询，解锁，批量解锁，强制下线。
- 支持用户在线统计，流量统计。
- 支持系统日志消息跟踪，帮助诊断用户故障。
- 支持WEB界面上网日志查询。
- 支持灵活的授权策略扩展。
- 支持多区域管理，操作员多区域关联支持，操作员与资费关联支持。
- 支持操作员权限分级管理。
- 支持第三方支付在线充值续费。
- 支持用户数据，财务数据，记账数据导出管理。
- 支持批量用户导入开户。
- 支持在线实时开通账号使用。
- 支持COA强制下线功能。
- 支持实时记账扣费。
- 支持全局与资费级别的自定义记账间隔下发
- 支持不同类型设备自动限速适配。
- 支持账号到期自动下线。
- 支持到期特定地址池下发。
- 支持到期提前通知，通过邮件，短信和webhook触发实现。
- 详细的操作日志记录，多条件查询。

## 快速指南

请参考 [ToughRADIUS 快速指南](http://docs.toughradius.net/toughradius_v2/quickstart.html)

## 社区支持

TOUGHRADIUS 网站：http://www.toughradius.org

TOUGHRADIUS 社区：https://forum.toughcloud.net

TOUGHRADIUS 博客：http://blog.toughradius.org

TOUGHRADIUS 文档: http://docs.toughradius.net

Github 项目源码: https://github.com/talkincode/ToughRADIUS

Github 文档源码: https://github.com/talkincode/ToughRADIUS-GitBook

QQ交流群组: 247860313 (使用交流)，487229323 (开发交流)

## 商业支持

请访问网站：https://www.toughstruct.com





