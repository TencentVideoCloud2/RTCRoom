# RTCRoom项目

## 简介
目前腾讯云提供了移动直播SDK，包括IOS、Android、小程序、windows、IE插件等多个平台，最直观的感受是能够做推流与拉流，如何使用此SDK做双向音视频与多人音视频？同时实现移动端、windows端、小程序、网页端等多端互通？通过一个统一的房间管理后台来分发推拉流地址，各终端实现此协议完成地址交换即可实现多人音视频，RTCRoom项目即为此解决方案。

RTCRoom 提供了单向、双人、多人音视频的整体解决方案，实现了iOS、Android、Windows、小程序等多终端互通，各终端Demo及服务端代码开源，有一套示例源码。其中客户端的源码主要是提供 CreateRoom、EnterRoom、ExitRoom 等进出房间的接口，而服务端源码则用于房间管理，并通过腾讯云通讯（IM）服务向房间内成员发送事件通知，目前服务端采用的NodeJS实现。

RTCRoom的小程序及后台方案基于腾讯云的 Wafer解决方案，该方案是与微信团队深度定制合作的一站式小程序解决方案，用户只需要开通，即可使用开发者工具上传、部署、调试小程序后端代码，无需了解服务器运维、数据库部署搭建即可使用。开发阶段用户不需要自行对服务器进行操作部署和上传代码，只需要下载安装微信开发者工具，并通过微信开发者工具一键上传、部署、调试小程序后端代码，即可通过腾讯云分配的域名访问，方便开发调试，后续上线客户需要根据自己的实际情况部署到客户的后台服务器。

各端SDK及demo下载请参考：

| 操作系统 | 下载链接 | 源码位置 |
|---------|---------|---------|
| 小程序 | [DOWNLOAD](https://cloud.tencent.com/document/product/454/7873#XiaoChengXu) | 小程序源码 zip 包中的 wxlite 文件夹 |
| 服务端 | [DOWNLOAD](https://cloud.tencent.com/document/product/454/7873#XiaoChengXu) | 小程序源码 zip 包中的 server 文件夹  |
| iOS | [DOWNLOAD](https://cloud.tencent.com/document/product/454/7873#iOS) | SDK 开发包 RtcRoom.m |
| Android | [DOWNLOAD](https://cloud.tencent.com/document/product/454/7873#Android) |  SDK 开发包 RtcRoom.java |
| Windows | [DOWNLOAD](https://cloud.tencent.com/document/product/454/7873#Windows) | Demo 源码中的 RTCRoom.h+RTCRoom.cpp |

## 项目方案及适用场景
### 单向音视频解决方案

![](https://mc.qcloudimg.com/static/img/6439160b7f1d0c0fc170e814d5b182c3/image.jpg)
   
  该方案详细交互流程图请参考：【待完善】
  该方案目前主要用于在线直播、在线培训、在线电玩类应用场景，具体参考[单向音视频应用场景](https://cloud.tencent.com/document/product/454/7873#iOS) 

### 双人与多人音视频解决方案
![多人音视频](https://mc.qcloudimg.com/static/img/619d515f6955ec3430caf6e7e7cd761d/image.jpg)
  
  该方案详细交互流程图请参考：[多人音视频交互图](https://mc.qcloudimg.com/static/img/a4aff101682c72db8ee5651a899034bb/RTX20171220-161158.png)
  该方案目前主要用于车险定损、客服类、多人会话、双人会话类应用场景，具体参考[双人多人会话应用场景](https://cloud.tencent.com/document/product/454/7873#iOS) 

## 开发者资源

 * [小程序与服务端部署指引](https://cloud.tencent.com/document/product/454/12554) - 一键部署小程序与服务端
 * 小程序
    - [项目结构](https://cloud.tencent.com/document/product/454/7873#iOS) - 小程序项目结构
    - [LocalView&RemoveView](https://cloud.tencent.com/document/product/454/7873#iOS) -       RTCRoom组件，用于双人、多人会话场景，基于RTCRoom API，更加易用
    - [RTCRoom API](https://cloud.tencent.com/document/product/454/7873#iOS) -       RTCRoom API文档，用于双人、多人会话场景，推荐使用LocalView&RemoveView组件
    - [LiveRoom API](https://cloud.tencent.com/document/product/454/7873#iOS) -       LiveRoom API文档，用于单向音视频场景
    - 原生标签使用
        - [live-pusher标签](https://cloud.tencent.com/document/product/454/12518) -       微信原生live-pusher标签使用文档
        - [live-player标签](https://cloud.tencent.com/document/product/454/12519) -       微信原生live-player标签使用文档
    - [常见问题](https://cloud.tencent.com/document/product/454/13037?!preview&lang=cn) -       小程序视频标签使用过程中常见问题
 * 服务端
    - [项目结构](https://cloud.tencent.com/document/product/454/7873#iOS) - 服务端项目结构及简介
    - [协议文档](https://cloud.tencent.com/document/product/454/7873#iOS) - 后台协议文档
    - [自行部署指引](https://cloud.tencent.com/document/product/454/7873#iOS) - 自己本地部署及服务端部署
    - [客户如何接入自有系统](https://cloud.tencent.com/document/product/454/7873#iOS) - 如何将现有的服务端代码接入客户自己的系统
 * 其他终端
  - [终端部署指引](https://cloud.tencent.com/document/product/454/7873#iOS) -       IE插件、windows、IOS、Android终端部署指引




