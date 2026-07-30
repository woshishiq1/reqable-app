# Reqable

[English](README.md) | [简体中文](README_CN.md) | [繁體中文](README_ZH-HANT.md) | [日本語](README_JA.md) | [한국어](README_KO.md) | [Español](README_ES.md) | [Français](README_FR.md) | [Deutsch](README_DE.md) | [Русский](README_RU.md)

⚠️ **注意：Reqable是非开源项目，本仓库仅用来管理需求和用户反馈。**

## 关于

[Reqable](https://reqable.com/) 是新一代API调试 + API测试一站化解决方案。Reqable具有全平台、免登录、轻量级、高性能、无广告等优点，理念是让API更快更简单，助力程序开发和测试人员提高生产力！现已支持 `Windows`、`Mac`、`Linux`、`Android` 和 `iOS` 五大平台。

Reqable = API抓包工具 + API测试工具，两者深度整合，抓测一体，操作简单，一个工具顶多个工具。

![](arts/products_zh.png)

Reqable 绝大多数功能均可免费使用，没有试用期限，社区版本适合轻度使用者；如果你是功能重度使用者，可能需要购买我们的高级会员。

欢迎访问我们的官方网站：https://reqable.com

## 目录

- [关于](#关于)
- [API调试](#api调试)
- [API测试](#api测试)
- [MCP支持](#mcp支持)
- [极致性能](#极致性能)
- [移动端版本](#移动端版本)
- [安装](#安装)
- [使用文档](#使用文档)
- [致谢](#致谢)

# API调试

Reqable采用经典的MITM（中间人）方式对HTTP(S)请求进行抓包，在桌面端使用系统代理的方式拦截流量，在移动端则使用VPN的方式拦截流量。Reqable支持对抓包数据进行调试操作，例如重放、编辑、断点、重写、脚本等。

![](arts/screenshot_zh_01.png)

# API测试

Reqable可以编辑、发送和管理 `HTTP`、`WebSocket`、`SSE` 和 `GRPC`（即将上线）请求，支持API集合，环境变量，文档管理和云同步等功能。

![](arts/screenshot_zh_02.png)

# MCP支持

Reqable提供了内置MCP服务器，你可以将 AI助手（如 Claude、Copilot）与 Reqable 连接起来，从而实现AI驱动的接口调试、流量分析、规则创建等功能。

![](arts/screenshot_zh_03.png)

MCP服务器代码我们是完全开源的，详见 [MCP Server](https://github.com/reqable/reqable-mcp-server)。

# 极致性能

Reqable基于Flutter和C++开发，拒绝内置浏览器，不仅安全性高，相比同类产品还具有极大的性能优势。

- 速度快，毫秒级启动。
- 安装空间小，不足100M。
- 内存占用低，日常低于300M。

抓包工具性能指标

![](arts/benchmark_zh_02.png)

接口工具性能指标

![](arts/benchmark_zh_01.png)

> 以上数据是在苹果最新的MacBook Pro M5设备上的测试结果，在硬件性能较差的设备上，Reqable的性能优势更加明显。

# 移动端版本

移动端和桌面端功能基本保持一致，同时支持API调试和API测试。同时，支持手机扫码添加电脑设备，将手机流量转发到电脑端进行操作。

登录后启用云端数据存储，可以在不同设备之间自动同步数据。

![](arts/screenshot_zh_04.png)

> 断点、重写和脚本功能担心引起滥用暂未上线。

# 安装

|  平台 | 架构 | 格式 | 下载&安装  | 说明  |
| ----  | ----  | ----  | ----  | ----  |
| **Windows** | x86_64 | exe | [下载](https://app.reqable.com/download?platform=windows&arch=x86_64&ext=exe&locale=zh-CN) | 安装版本（建议），支持 `Windows 7+`。 |
| **Windows** | x86_64 | zip | [下载](https://app.reqable.com/download?platform=windows&arch=x86_64&ext=zip&locale=zh-CN) | 免安装版本，支持 `Windows 7+`。 |
| **Mac** | universal | - |  brew install reqable | 要求系统 `11.0` 及以上版本。 |
| **Mac** | Intel Chip | dmg | [下载](https://app.reqable.com/download?platform=macos&arch=x86_64&ext=dmg&locale=zh-CN) | Intel芯片，要求系统 `11.0` 及以上版本。 |
| **Mac** | Apple Silicon |  dmg | [下载](https://app.reqable.com/download?platform=macos&arch=arm64&ext=dmg&locale=zh-CN) | M系列芯片，要求系统 `11.0` 及以上版本。 |
| **Linux** | x86_64 | deb | [下载](https://app.reqable.com/download?platform=linux&arch=x86_64&ext=deb&locale=zh-CN) | 支持 `Ubuntu` 和 `Debian` 等发行版本，并要求安装 `GTK 3.0`。|
| **Linux** | x86_64 | AppImage |[下载](https://app.reqable.com/download?platform=linux&arch=x86_64&ext=AppImage&locale=zh-CN) | 支持 `Ubuntu` 和 `Debian` 等发行版本，并要求安装 `GTK 3.0`。|
| **Android** | universal |  - |  [Google Play](https://play.google.com/store/apps/details?id=com.reqable.android) | 要求 `Android 5.0` 及以上系统版本。 |
| **Android** | arm64-v8a |  apk |  [下载](https://app.reqable.com/download?platform=android&arch=arm64&ext=apk&locale=zh-CN) | 要求 `Android 5.0` 及以上系统版本。  |
| **Android** | armeabi-v7a |  apk |  [下载](https://app.reqable.com/download?platform=android&arch=arm&ext=apk&locale=zh-CN) | 要求 `Android 5.0` 及以上系统版本。 |
| **Android** | x86_64 |  apk |  [下载](https://app.reqable.com/download?platform=android&arch=x86_64&ext=apk&locale=zh-CN) | 要求 `Android 5.0` 及以上系统版本。 |
| **iOS** | arm64 |  - |  [App Store](https://apps.apple.com/cn/app/id6473166828) | 要求 `iOS 13.0` 及以上系统版本。 |

## 使用文档
https://reqable.com/zh-CN/docs/introduction

## 致谢

<p align="left">
  <a href="https://github.com/RonaldinhoL" title="RonaldinhoL (51 issues)"><img src="https://avatars.githubusercontent.com/u/1797392?v=4&amp;s=80" width="40" height="40" alt="RonaldinhoL" /></a>
  <a href="https://github.com/cesuproxy" title="cesuproxy (49 issues)"><img src="https://avatars.githubusercontent.com/u/195559109?v=4&amp;s=80" width="40" height="40" alt="cesuproxy" /></a>
  <a href="https://github.com/zclovelyj" title="zclovelyj (23 issues)"><img src="https://avatars.githubusercontent.com/u/38125286?v=4&amp;s=80" width="40" height="40" alt="zclovelyj" /></a>
  <a href="https://github.com/xiuluoshendaren" title="xiuluoshendaren (21 issues)"><img src="https://avatars.githubusercontent.com/u/160598517?v=4&amp;s=80" width="40" height="40" alt="xiuluoshendaren" /></a>
  <a href="https://github.com/hhs66317" title="hhs66317 (18 issues)"><img src="https://avatars.githubusercontent.com/u/3916247?v=4&amp;s=80" width="40" height="40" alt="hhs66317" /></a>
  <a href="https://github.com/DemonZD" title="DemonZD (14 issues)"><img src="https://avatars.githubusercontent.com/u/91039854?v=4&amp;s=80" width="40" height="40" alt="DemonZD" /></a>
  <a href="https://github.com/xuennai" title="xuennai (13 issues)"><img src="https://avatars.githubusercontent.com/u/63104635?v=4&amp;s=80" width="40" height="40" alt="xuennai" /></a>
  <a href="https://github.com/NavinChen" title="NavinChen (12 issues)"><img src="https://avatars.githubusercontent.com/u/11780577?v=4&amp;s=80" width="40" height="40" alt="NavinChen" /></a>
  <a href="https://github.com/ejfkdev" title="ejfkdev (12 issues)"><img src="https://avatars.githubusercontent.com/u/152914458?v=4&amp;s=80" width="40" height="40" alt="ejfkdev" /></a>
  <a href="https://github.com/QuanTum2088" title="QuanTum2088 (12 issues)"><img src="https://avatars.githubusercontent.com/u/158152582?v=4&amp;s=80" width="40" height="40" alt="QuanTum2088" /></a>
  <a href="https://github.com/DreamlingBig" title="DreamlingBig (11 issues)"><img src="https://avatars.githubusercontent.com/u/44178151?v=4&amp;s=80" width="40" height="40" alt="DreamlingBig" /></a>
  <a href="https://github.com/cesaryuan" title="cesaryuan (10 issues)"><img src="https://avatars.githubusercontent.com/u/35998162?v=4&amp;s=80" width="40" height="40" alt="cesaryuan" /></a>
  <a href="https://github.com/am3k0" title="am3k0 (10 issues)"><img src="https://avatars.githubusercontent.com/u/71699483?v=4&amp;s=80" width="40" height="40" alt="am3k0" /></a>
  <a href="https://github.com/xvhuan" title="xvhuan (10 issues)"><img src="https://avatars.githubusercontent.com/u/50939413?v=4&amp;s=80" width="40" height="40" alt="xvhuan" /></a>
  <a href="https://github.com/picture-j" title="picture-j (10 issues)"><img src="https://avatars.githubusercontent.com/u/62652474?v=4&amp;s=80" width="40" height="40" alt="picture-j" /></a>
  <a href="https://github.com/cxplay" title="cxplay (9 issues)"><img src="https://avatars.githubusercontent.com/u/62034099?v=4&amp;s=80" width="40" height="40" alt="cxplay" /></a>
  <a href="https://github.com/SugarFatFree" title="SugarFatFree (9 issues)"><img src="https://avatars.githubusercontent.com/u/30424828?v=4&amp;s=80" width="40" height="40" alt="SugarFatFree" /></a>
  <a href="https://github.com/ghost" title="ghost (9 issues)"><img src="https://avatars.githubusercontent.com/u/10137?v=4&amp;s=80" width="40" height="40" alt="ghost" /></a>
  <a href="https://github.com/Lehcok" title="Lehcok (9 issues)"><img src="https://avatars.githubusercontent.com/u/63954316?v=4&amp;s=80" width="40" height="40" alt="Lehcok" /></a>
  <a href="https://github.com/19774279" title="19774279 (9 issues)"><img src="https://avatars.githubusercontent.com/u/3414408?v=4&amp;s=80" width="40" height="40" alt="19774279" /></a>
  <a href="https://github.com/Jingle-Pan" title="Jingle-Pan (9 issues)"><img src="https://avatars.githubusercontent.com/u/75921710?v=4&amp;s=80" width="40" height="40" alt="Jingle-Pan" /></a>
  <a href="https://github.com/nullCode666" title="nullCode666 (9 issues)"><img src="https://avatars.githubusercontent.com/u/82703497?v=4&amp;s=80" width="40" height="40" alt="nullCode666" /></a>
  <a href="https://github.com/gyunlyun" title="gyunlyun (9 issues)"><img src="https://avatars.githubusercontent.com/u/111403418?v=4&amp;s=80" width="40" height="40" alt="gyunlyun" /></a>
  <a href="https://github.com/Arcticlyc" title="Arcticlyc (8 issues)"><img src="https://avatars.githubusercontent.com/u/94273547?v=4&amp;s=80" width="40" height="40" alt="Arcticlyc" /></a>
  <a href="https://github.com/TopMaps" title="TopMaps (8 issues)"><img src="https://avatars.githubusercontent.com/u/163238823?v=4&amp;s=80" width="40" height="40" alt="TopMaps" /></a>
  <a href="https://github.com/pansy1110" title="pansy1110 (8 issues)"><img src="https://avatars.githubusercontent.com/u/118948488?v=4&amp;s=80" width="40" height="40" alt="pansy1110" /></a>
  <a href="https://github.com/cry980285208" title="cry980285208 (8 issues)"><img src="https://avatars.githubusercontent.com/u/46832863?v=4&amp;s=80" width="40" height="40" alt="cry980285208" /></a>
  <a href="https://github.com/Toskysun" title="Toskysun (8 issues)"><img src="https://avatars.githubusercontent.com/u/88605463?v=4&amp;s=80" width="40" height="40" alt="Toskysun" /></a>
  <a href="https://github.com/Acheng97" title="Acheng97 (7 issues)"><img src="https://avatars.githubusercontent.com/u/65265814?v=4&amp;s=80" width="40" height="40" alt="Acheng97" /></a>
  <a href="https://github.com/lsdlh" title="lsdlh (7 issues)"><img src="https://avatars.githubusercontent.com/u/45959509?v=4&amp;s=80" width="40" height="40" alt="lsdlh" /></a>
  <a href="https://github.com/CAI5201314" title="CAI5201314 (7 issues)"><img src="https://avatars.githubusercontent.com/u/155355247?v=4&amp;s=80" width="40" height="40" alt="CAI5201314" /></a>
  <a href="https://github.com/86523553" title="86523553 (7 issues)"><img src="https://avatars.githubusercontent.com/u/72677878?v=4&amp;s=80" width="40" height="40" alt="86523553" /></a>
  <a href="https://github.com/Jesn" title="Jesn (7 issues)"><img src="https://avatars.githubusercontent.com/u/5728274?v=4&amp;s=80" width="40" height="40" alt="Jesn" /></a>
  <a href="https://github.com/zsh2517" title="zsh2517 (7 issues)"><img src="https://avatars.githubusercontent.com/u/30528671?v=4&amp;s=80" width="40" height="40" alt="zsh2517" /></a>
  <a href="https://github.com/CHINA-T" title="CHINA-T (7 issues)"><img src="https://avatars.githubusercontent.com/u/54023741?v=4&amp;s=80" width="40" height="40" alt="CHINA-T" /></a>
  <a href="https://github.com/1002753959" title="1002753959 (7 issues)"><img src="https://avatars.githubusercontent.com/u/31638769?v=4&amp;s=80" width="40" height="40" alt="1002753959" /></a>
  <a href="https://github.com/hyt65098631" title="hyt65098631 (6 issues)"><img src="https://avatars.githubusercontent.com/u/83172030?v=4&amp;s=80" width="40" height="40" alt="hyt65098631" /></a>
  <a href="https://github.com/yinsel" title="yinsel (6 issues)"><img src="https://avatars.githubusercontent.com/u/91541985?v=4&amp;s=80" width="40" height="40" alt="yinsel" /></a>
  <a href="https://github.com/xx299x" title="xx299x (6 issues)"><img src="https://avatars.githubusercontent.com/u/23482348?v=4&amp;s=80" width="40" height="40" alt="xx299x" /></a>
  <a href="https://github.com/wuewill" title="wuewill (6 issues)"><img src="https://avatars.githubusercontent.com/u/136971925?v=4&amp;s=80" width="40" height="40" alt="wuewill" /></a>
  <a href="https://github.com/jinshuqishi2019" title="jinshuqishi2019 (6 issues)"><img src="https://avatars.githubusercontent.com/u/57516638?v=4&amp;s=80" width="40" height="40" alt="jinshuqishi2019" /></a>
  <a href="https://github.com/TopChina" title="TopChina (6 issues)"><img src="https://avatars.githubusercontent.com/u/11971348?v=4&amp;s=80" width="40" height="40" alt="TopChina" /></a>
  <a href="https://github.com/Dawnnnnnn" title="Dawnnnnnn (6 issues)"><img src="https://avatars.githubusercontent.com/u/24506421?v=4&amp;s=80" width="40" height="40" alt="Dawnnnnnn" /></a>
  <a href="https://github.com/Mrqqeat" title="Mrqqeat (6 issues)"><img src="https://avatars.githubusercontent.com/u/12445017?v=4&amp;s=80" width="40" height="40" alt="Mrqqeat" /></a>
  <a href="https://github.com/Soujer" title="Soujer (6 issues)"><img src="https://avatars.githubusercontent.com/u/43666892?v=4&amp;s=80" width="40" height="40" alt="Soujer" /></a>
  <a href="https://github.com/fankuiz6" title="fankuiz6 (6 issues)"><img src="https://avatars.githubusercontent.com/u/156877102?v=4&amp;s=80" width="40" height="40" alt="fankuiz6" /></a>
  <a href="https://github.com/airline233" title="airline233 (6 issues)"><img src="https://avatars.githubusercontent.com/u/70080598?v=4&amp;s=80" width="40" height="40" alt="airline233" /></a>
</p>
