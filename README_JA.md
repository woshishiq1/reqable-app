# Reqable

[English](README.md) | [简体中文](README_CN.md) | [繁體中文](README_ZH-HANT.md) | [日本語](README_JA.md) | [한국어](README_KO.md) | [Español](README_ES.md) | [Français](README_FR.md) | [Deutsch](README_DE.md) | [Русский](README_RU.md)

⚠️ **注意：Reqable はオープンソースプロジェクトではありません。このリポジトリはニーズ管理とユーザーフィードバックのみに使用されます。**

## 概要

[Reqable](https://reqable.com/) は新世代の API デバッグ + API テストのワンストップソリューションです。Reqable は全プラットフォーム対応、ログイン不要、軽量、高性能、広告なしといった特長を持ち、「API をより速く、よりシンプルに」を理念に、開発者とテスターの生産性向上を支援します。現在、`Windows`、`Mac`、`Linux`、`Android`、`iOS` の 5 大プラットフォームに対応しています。

Reqable = API キャプチャツール + API テストツール。両者を深く統合し、キャプチャとテストを一体化。シンプルな操作で、1 つのツールが複数のツールの役割を果たします。

![](arts/products_en.png)

Reqable のほとんどの機能は無料で使用でき、試用期限はありません。コミュニティ版はライトユーザーに適しています。ヘビーユーザーの場合は、プレミアム会員の購入が必要になることがあります。

公式ウェブサイトをご覧ください：https://reqable.com

## 目次

- [概要](#概要)
- [API デバッグ](#api-デバッグ)
- [API テスト](#api-テスト)
- [MCP サポート](#mcp-サポート)
- [究極のパフォーマンス](#究極のパフォーマンス)
- [モバイルアプリ](#モバイルアプリ)
- [インストール](#インストール)
- [ドキュメント](#ドキュメント)
- [謝辞](#謝辞)

# API デバッグ

Reqable はクラシックな MITM（中間者）方式で HTTP(S) リクエストをキャプチャします。デスクトップではシステムプロキシを使用してトラフィックを傍受し、モバイルでは VPN を使用します。Reqable はキャプチャデータのデバッグ操作（再送、編集、ブレークポイント、リライト、スクリプトなど）をサポートしています。

![](arts/screenshot_en_01.png)

# API テスト

Reqable は `HTTP`、`WebSocket`、`SSE`、`gRPC`（近日リリース予定）リクエストの編集、送信、管理が可能で、API コレクション、環境変数、ドキュメント管理、クラウド同期などの機能をサポートしています。

![](arts/screenshot_en_02.png)

# MCP サポート

Reqable は内蔵 MCP サーバーを提供し、AI アシスタント（Claude、Copilot など）を Reqable に接続することで、AI 駆動の API デバッグ、トラフィック分析、ルール作成などを実現できます。

![](arts/screenshot_en_03.png)

MCP サーバーのコードは完全にオープンソースです。詳細は [MCP Server](https://github.com/reqable/reqable-mcp-server) をご覧ください。

# 究極のパフォーマンス

Reqable は Flutter と C++ で開発され、ブラウザの組み込みを排除しています。これにより高いセキュリティを実現するだけでなく、同類製品と比較して圧倒的なパフォーマンス優位性を持っています。

- 高速、ミリ秒レベルの起動。
- インストールサイズが小さく、100M 未満。
- メモリ使用量が低く、日常的に 300M 未満。

パケットキャプチャパフォーマンスベンチマーク

![](arts/benchmark_en_02.png)

API クライアントパフォーマンスベンチマーク

![](arts/benchmark_en_01.png)

> ベンチマークは M5 チップ搭載の Apple MacBook Pro で実施されました。ハードウェア性能の低いデバイスでは、Reqable のパフォーマンス優位性がさらに顕著になります。

# モバイルアプリ

モバイル版とデスクトップ版の機能はほぼ同等で、API デバッグと API テストの両方をサポートしています。また、QR コードをスキャンしてパソコンを追加し、モバイルトラフィックをパソコンに転送して操作することができます。

ログイン後にクラウドデータストレージを有効にすると、異なるデバイス間でデータを自動同期できます。

![](arts/screenshot_en_04.png)

> ブレークポイント、リライト、スクリプト機能は悪用の懸念があるため、現在提供されていません。

# インストール

| プラットフォーム | アーキテクチャ | 形式 | ダウンロードとインストール | 備考 |
| ---- | ---- | ---- | ---- | ---- |
| **Windows** | x86_64 | exe | [ダウンロード](https://app.reqable.com/download?platform=windows&arch=x86_64&ext=exe&locale=en-US) | インストーラ版（推奨）、`Windows 7+` 対応。 |
| **Windows** | x86_64 | zip | [ダウンロード](https://app.reqable.com/download?platform=windows&arch=x86_64&ext=zip&locale=en-US) | ポータブル版、`Windows 7+` 対応。 |
| **Mac** | universal | - | brew install reqable | macOS `11.0` 以降が必要。 |
| **Mac** | Intel Chip | dmg | [ダウンロード](https://app.reqable.com/download?platform=macos&arch=x86_64&ext=dmg&locale=en-US) | Intel チップ、macOS `11.0` 以降が必要。 |
| **Mac** | Apple Silicon | dmg | [ダウンロード](https://app.reqable.com/download?platform=macos&arch=arm64&ext=dmg&locale=en-US) | M シリーズチップ、macOS `11.0` 以降が必要。 |
| **Linux** | x86_64 | deb | [ダウンロード](https://app.reqable.com/download?platform=linux&arch=x86_64&ext=deb&locale=en-US) | `Ubuntu`、`Debian` などのディストリビューションに対応。`GTK 3.0` が必要。 |
| **Linux** | x86_64 | AppImage | [ダウンロード](https://app.reqable.com/download?platform=linux&arch=x86_64&ext=AppImage&locale=en-US) | `Ubuntu`、`Debian` などのディストリビューションに対応。`GTK 3.0` が必要。 |
| **Android** | universal | - | [Google Play](https://play.google.com/store/apps/details?id=com.reqable.android) | `Android 5.0` 以降が必要。 |
| **Android** | arm64-v8a | apk | [ダウンロード](https://app.reqable.com/download?platform=android&arch=arm64&ext=apk&locale=en-US) | `Android 5.0` 以降が必要。 |
| **Android** | armeabi-v7a | apk | [ダウンロード](https://app.reqable.com/download?platform=android&arch=arm&ext=apk&locale=en-US) | `Android 5.0` 以降が必要。 |
| **Android** | x86_64 | apk | [ダウンロード](https://app.reqable.com/download?platform=android&arch=x86_64&ext=apk&locale=en-US) | `Android 5.0` 以降が必要。 |
| **iOS** | arm64 | - | [App Store](https://apps.apple.com/cn/app/id6473166828) | `iOS 13.0` 以降が必要。 |

## ドキュメント
https://reqable.com/en-US/docs/introduction

## 謝辞

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
