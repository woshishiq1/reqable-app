# Reqable

[English](README.md) | [简体中文](README_CN.md) | [繁體中文](README_ZH-HANT.md) | [日本語](README_JA.md) | [한국어](README_KO.md) | [Español](README_ES.md) | [Français](README_FR.md) | [Deutsch](README_DE.md) | [Русский](README_RU.md)

⚠️ **注意：Reqable 非開源專案，本倉庫僅用來管理需求與使用者回饋。**

## 關於

[Reqable](https://reqable.com/) 是新一代 API 除錯 + API 測試一站化解決方案。Reqable 具有全平台、免登入、輕量級、高效能、無廣告等優點，理念是讓 API 更快更簡單，助力程式開發與測試人員提高生產力！現已支援 `Windows`、`Mac`、`Linux`、`Android` 和 `iOS` 五大平台。

Reqable = API 抓包工具 + API 測試工具，兩者深度整合，抓測一體，操作簡單，一個工具頂多個工具。

![](arts/products_en.png)

Reqable 絕大多數功能均可免費使用，沒有試用期限，社群版本適合輕度使用者；如果你是功能重度使用者，可能需要購買我們的高級會員。

歡迎造訪我們的官方網站：https://reqable.com

## 目錄

- [關於](#關於)
- [API 除錯](#api-除錯)
- [API 測試](#api-測試)
- [MCP 支援](#mcp-支援)
- [極致效能](#極致效能)
- [行動版 App](#行動版-app)
- [安裝](#安裝)
- [文件](#文件)
- [致謝](#致謝)

# API 除錯

Reqable 採用經典的 MITM（中間人）方式對 HTTP(S) 請求進行抓包，在桌面端使用系統代理的方式攔截流量，在移動端則使用 VPN 的方式攔截流量。Reqable 支援對抓包資料進行除錯操作，例如重放、編輯、中斷點、重寫、指令碼等。

![](arts/screenshot_en_01.png)

# API 測試

Reqable 可以編輯、傳送和管理 `HTTP`、`WebSocket`、`SSE` 和 `gRPC`（即將上線）請求，支援 API 集合、環境變數、文件管理和雲端同步等功能。

![](arts/screenshot_en_02.png)

# MCP 支援

Reqable 提供了內建 MCP 伺服器，你可以將 AI 助手（如 Claude、Copilot）與 Reqable 連接起來，從而實現 AI 驅動的介面除錯、流量分析、規則建立等功能。

![](arts/screenshot_en_03.png)

MCP 伺服器程式碼我們是完全開源的，詳見 [MCP Server](https://github.com/reqable/reqable-mcp-server)。

# 極致效能

Reqable 基於 Flutter 和 C++ 開發，拒絕內建瀏覽器，不僅安全性高，相比同類產品還具有極大的效能優勢。

- 速度快，毫秒級啟動。
- 安裝空間小，不足 100M。
- 記憶體占用低，日常低於 300M。

封包擷取效能基準測試

![](arts/benchmark_en_02.png)

API 用戶端效能基準測試

![](arts/benchmark_en_01.png)

> 以上資料是在蘋果最新的 MacBook Pro M5 裝置上的測試結果，在硬體效能較差的裝置上，Reqable 的效能優勢更加明顯。

# 行動版 App

行動端和桌面端功能基本保持一致，同時支援 API 除錯和 API 測試。同時，支援手機掃碼新增電腦裝置，將手機流量轉發到電腦端進行操作。

登入後啟用雲端資料儲存，可以在不同裝置之間自動同步資料。

![](arts/screenshot_en_04.png)

> 中斷點、重寫和指令碼功能擔心引起濫用暫未上線。

# 安裝

| 平台 | 架構 | 格式 | 下載與安裝 | 說明 |
| ---- | ---- | ---- | ---- | ---- |
| **Windows** | x86_64 | exe | [下載](https://app.reqable.com/download?platform=windows&arch=x86_64&ext=exe&locale=en-US) | 安裝程式版本（建議），支援 `Windows 7+`。 |
| **Windows** | x86_64 | zip | [下載](https://app.reqable.com/download?platform=windows&arch=x86_64&ext=zip&locale=en-US) | 可攜式版本，支援 `Windows 7+`。 |
| **Mac** | universal | - | brew install reqable | 需要 macOS `11.0` 或更新版本。 |
| **Mac** | Intel Chip | dmg | [下載](https://app.reqable.com/download?platform=macos&arch=x86_64&ext=dmg&locale=en-US) | Intel 晶片，需要 macOS `11.0` 或更新版本。 |
| **Mac** | Apple Silicon | dmg | [下載](https://app.reqable.com/download?platform=macos&arch=arm64&ext=dmg&locale=en-US) | M 系列晶片，需要 macOS `11.0` 或更新版本。 |
| **Linux** | x86_64 | deb | [下載](https://app.reqable.com/download?platform=linux&arch=x86_64&ext=deb&locale=en-US) | 支援 `Ubuntu`、`Debian` 及其他發行版。需要 `GTK 3.0`。 |
| **Linux** | x86_64 | AppImage | [下載](https://app.reqable.com/download?platform=linux&arch=x86_64&ext=AppImage&locale=en-US) | 支援 `Ubuntu`、`Debian` 及其他發行版。需要 `GTK 3.0`。 |
| **Android** | universal | - | [Google Play](https://play.google.com/store/apps/details?id=com.reqable.android) | 需要 `Android 5.0` 或更新版本。 |
| **Android** | arm64-v8a | apk | [下載](https://app.reqable.com/download?platform=android&arch=arm64&ext=apk&locale=en-US) | 需要 `Android 5.0` 或更新版本。 |
| **Android** | armeabi-v7a | apk | [下載](https://app.reqable.com/download?platform=android&arch=arm&ext=apk&locale=en-US) | 需要 `Android 5.0` 或更新版本。 |
| **Android** | x86_64 | apk | [下載](https://app.reqable.com/download?platform=android&arch=x86_64&ext=apk&locale=en-US) | 需要 `Android 5.0` 或更新版本。 |
| **iOS** | arm64 | - | [App Store](https://apps.apple.com/cn/app/id6473166828) | 需要 `iOS 13.0` 或更新版本。 |

## 文件
https://reqable.com/en-US/docs/introduction

## 致謝

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
