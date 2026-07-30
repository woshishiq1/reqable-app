# Reqable

[English](README.md) | [简体中文](README_CN.md) | [繁體中文](README_ZH-HANT.md) | [日本語](README_JA.md) | [한국어](README_KO.md) | [Español](README_ES.md) | [Français](README_FR.md) | [Deutsch](README_DE.md) | [Русский](README_RU.md)

⚠️ **참고: Reqable은 오픈소스 프로젝트가 아닙니다. 이 저장소는 요구사항 관리와 사용자 피드백 용도로만 사용됩니다.**

## 소개

[Reqable](https://reqable.com/)은 차세대 API 디버깅 + API 테스트 원스톱 솔루션입니다. Reqable은 전 플랫폼 지원, 로그인 불필요, 가볍고, 고성능, 광고 없음 등의 장점을 갖추고 있으며, API를 더 빠르고 간단하게 만들어 개발자와 테스터의 생산성을 높이는 것을 목표로 합니다. 현재 `Windows`, `Mac`, `Linux`, `Android`, `iOS` 5대 플랫폼을 지원합니다.

Reqable = API 캡처 도구 + API 테스트 도구. 양자를 긴밀하게 통합하여 캡처와 테스트를 일체화했으며, 조작이 간단해 하나의 도구로 여러 도구를 대체합니다.

![](arts/products_en.png)

Reqable의 대부분의 기능은 무료로 사용할 수 있으며 평가판 기간이 없습니다. 커뮤니티 버전은 라이트 유저에게 적합합니다. 헤비 유저라면 프리미엄 멤버십 구매가 필요할 수 있습니다.

공식 웹사이트 방문: https://reqable.com

## 목차

- [소개](#소개)
- [API 디버깅](#api-디버깅)
- [API 테스트](#api-테스트)
- [MCP 지원](#mcp-지원)
- [극한의 성능](#극한의-성능)
- [모바일 앱](#모바일-앱)
- [설치](#설치)
- [문서](#문서)
- [감사의 말](#감사의-말)

# API 디버깅

Reqable은 클래식 MITM(중간자) 방식으로 HTTP(S) 요청을 캡처합니다. 데스크톱에서는 시스템 프록시를 사용하여 트래픽을 가로채고, 모바일에서는 VPN을 사용합니다. Reqable은 캡처 데이터에 대한 디버깅 작업(재전송, 편집, 중단점, 재작성, 스크립팅 등)을 지원합니다.

![](arts/screenshot_en_01.png)

# API 테스트

Reqable은 `HTTP`, `WebSocket`, `SSE`, `gRPC`(곧 출시 예정) 요청을 편집, 전송, 관리할 수 있으며, API 컬렉션, 환경 변수, 문서 관리, 클라우드 동기화 등의 기능을 지원합니다.

![](arts/screenshot_en_02.png)

# MCP 지원

Reqable은 내장 MCP 서버를 제공하여 AI 어시스턴트(Claude, Copilot 등)를 Reqable에 연결함으로써, AI 기반 API 디버깅, 트래픽 분석, 규칙 생성 등을 실현할 수 있습니다.

![](arts/screenshot_en_03.png)

MCP 서버 코드는 완전히 오픈소스입니다. 자세한 내용은 [MCP Server](https://github.com/reqable/reqable-mcp-server)를 참조하세요.

# 극한의 성능

Reqable은 Flutter와 C++로 개발되었으며, 브라우저 내장을 배제했습니다. 이로 인해 높은 보안성을 갖추었을 뿐만 아니라, 동종 제품 대비 뛰어난 성능 우위를 자랑합니다.

- 빠른 속도, 밀리초 수준의 시작.
- 설치 공간이 작아 100M 미만.
- 메모리 사용량이 낮아 평소 300M 미만.

패킷 캡처 성능 벤치마크

![](arts/benchmark_en_02.png)

API 클라이언트 성능 벤치마크

![](arts/benchmark_en_01.png)

> 벤치마크는 M5 칩이 탑재된 Apple MacBook Pro에서 수행되었습니다. 하드웨어 성능이 낮은 기기에서는 Reqable의 성능 우위가 더욱 두드러집니다.

# 모바일 앱

모바일 버전과 데스크톱 버전의 기능은 거의 동일하며, API 디버깅과 API 테스트를 모두 지원합니다. 또한 QR 코드를 스캔하여 PC 기기를 추가하고, 모바일 트래픽을 PC로 전달하여 작업할 수 있습니다.

로그인 후 클라우드 데이터 저장을 활성화하면, 서로 다른 기기 간에 데이터를 자동으로 동기화할 수 있습니다.

![](arts/screenshot_en_04.png)

> 중단점, 재작성 및 스크립팅 기능은 악용 우려로 인해 현재 제공되지 않습니다.

# 설치

| 플랫폼 | 아키텍처 | 형식 | 다운로드 및 설치 | 비고 |
| ---- | ---- | ---- | ---- | ---- |
| **Windows** | x86_64 | exe | [다운로드](https://app.reqable.com/download?platform=windows&arch=x86_64&ext=exe&locale=en-US) | 설치 관리자 버전(권장), `Windows 7+` 지원. |
| **Windows** | x86_64 | zip | [다운로드](https://app.reqable.com/download?platform=windows&arch=x86_64&ext=zip&locale=en-US) | 휴대용 버전, `Windows 7+` 지원. |
| **Mac** | universal | - | brew install reqable | macOS `11.0` 이상 필요. |
| **Mac** | Intel Chip | dmg | [다운로드](https://app.reqable.com/download?platform=macos&arch=x86_64&ext=dmg&locale=en-US) | Intel 칩, macOS `11.0` 이상 필요. |
| **Mac** | Apple Silicon | dmg | [다운로드](https://app.reqable.com/download?platform=macos&arch=arm64&ext=dmg&locale=en-US) | M 시리즈 칩, macOS `11.0` 이상 필요. |
| **Linux** | x86_64 | deb | [다운로드](https://app.reqable.com/download?platform=linux&arch=x86_64&ext=deb&locale=en-US) | `Ubuntu`, `Debian` 등 배포판 지원. `GTK 3.0` 필요. |
| **Linux** | x86_64 | AppImage | [다운로드](https://app.reqable.com/download?platform=linux&arch=x86_64&ext=AppImage&locale=en-US) | `Ubuntu`, `Debian` 등 배포판 지원. `GTK 3.0` 필요. |
| **Android** | universal | - | [Google Play](https://play.google.com/store/apps/details?id=com.reqable.android) | `Android 5.0` 이상 필요. |
| **Android** | arm64-v8a | apk | [다운로드](https://app.reqable.com/download?platform=android&arch=arm64&ext=apk&locale=en-US) | `Android 5.0` 이상 필요. |
| **Android** | armeabi-v7a | apk | [다운로드](https://app.reqable.com/download?platform=android&arch=arm&ext=apk&locale=en-US) | `Android 5.0` 이상 필요. |
| **Android** | x86_64 | apk | [다운로드](https://app.reqable.com/download?platform=android&arch=x86_64&ext=apk&locale=en-US) | `Android 5.0` 이상 필요. |
| **iOS** | arm64 | - | [App Store](https://apps.apple.com/cn/app/id6473166828) | `iOS 13.0` 이상 필요. |

## 문서
https://reqable.com/en-US/docs/introduction

## 감사의 말

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
