# Reqable

[English](README.md) | [简体中文](README_CN.md) | [繁體中文](README_ZH-HANT.md) | [日本語](README_JA.md) | [한국어](README_KO.md) | [Español](README_ES.md) | [Français](README_FR.md) | [Deutsch](README_DE.md) | [Русский](README_RU.md)

⚠️ **Hinweis: Reqable ist kein Open-Source-Projekt. Dieses Repository dient ausschließlich der Problemverfolgung, Funktionsanfragen und Benutzerfeedback.**

## Über

[Reqable](https://reqable.com/) ist eine All-in-One-Plattform der nächsten Generation für API-Debugging und -Tests. Sie bietet plattformübergreifende Unterstützung, eine anmeldefreie Architektur, einen geringen Ressourcenverbrauch, hohen Durchsatz und ein werbefreies Erlebnis — alles darauf ausgelegt, API-Workflows für Entwickler und QA-Ingenieure zu optimieren. Reqable unterstützt fünf große Plattformen: `Windows`, `macOS`, `Linux`, `Android` und `iOS`.

Reqable vereint ein API-Traffic-Capture-Tool mit einem voll ausgestatteten API-Testclient in einer einzigen, tief integrierten Umgebung — für nahtlose Capture-and-Test-Workflows und als Ersatz für mehrere eigenständige Tools.

![](arts/products_en.png)

Der Großteil der Funktionen von Reqable ist kostenlos und ohne Testzeitraum verfügbar. Die Community Edition deckt die Anforderungen der meisten Einzelentwickler ab; Power-User und Teams können von einem Upgrade auf die Premium-Stufe profitieren, um erweiterte Funktionen zu erhalten.

Besuchen Sie unsere offizielle Website: https://reqable.com

## Inhaltsverzeichnis

- [Über](#über)
- [API-Debugging](#api-debugging)
- [API-Tests](#api-tests)
- [MCP-Unterstützung](#mcp-unterstützung)
- [Extreme Performance](#extreme-performance)
- [Mobile App](#mobile-app)
- [Installation](#installation)
- [Dokumentation](#dokumentation)
- [Danksagungen](#danksagungen)

# API-Debugging

Reqable setzt auf eine klassische MITM-Strategie (Man-in-the-Middle), um HTTP(S)-Traffic abzufangen. Auf Desktop-Plattformen erfasst es den Traffic über systemweite Proxy-Konfiguration; auf Mobilgeräten nutzt es ein lokales VPN. Der erfasste Traffic kann mithilfe einer umfangreichen Sammlung von Debugging-Primitiven inspiziert und manipuliert werden: Request-Wiederholung, Inline-Bearbeitung, Haltepunkte, URL-Rewriting, benutzerdefiniertes Scripting und mehr.

![](arts/screenshot_en_01.png)

# API-Tests

Reqable bietet einen voll ausgestatteten API-Client zum Erstellen, Senden und Organisieren von `HTTP`-, `WebSocket`-, `SSE`- und `gRPC`-Anfragen (demnächst verfügbar). Er umfasst ordnerbasierte API-Sammlungen, Umgebungsvariablen mit Bereichsauflösung, integrierte API-Dokumentationserstellung sowie Cloud-Synchronisation über Geräte hinweg.

![](arts/screenshot_en_02.png)

# MCP-Unterstützung

Reqable verfügt über einen integrierten MCP-Server (Model Context Protocol), der es KI-Assistenten wie Claude und GitHub Copilot ermöglicht, direkt mit Reqable zu interagieren. Dies erschließt KI-gestützte Workflows für API-Debugging, Traffic-Inspektion, Regelerstellung und automatisierte Tests.

![](arts/screenshot_en_03.png)

Die MCP-Server-Implementierung ist vollständig quelloffen. Weitere Details finden Sie im [MCP Server Repository](https://github.com/reqable/reqable-mcp-server).

# Extreme Performance

Reqable wurde mit Flutter und C++ entwickelt und verzichtet bewusst auf eine eingebettete Browser-Laufzeitumgebung. Diese architektonische Entscheidung stärkt die Sicherheit durch Reduzierung der Angriffsfläche und bietet gleichzeitig erhebliche Leistungsvorteile gegenüber Electron-basierten Alternativen.

- Kaltstartzeit im Millisekundenbereich.
- Installationsgröße unter 100 MB.
- Typische Speichernutzung unter 300 MB bei aktiver Nutzung.

Paketerfassungs-Leistungsbenchmarks

![](arts/benchmark_en_02.png)

API-Client-Leistungsbenchmarks

![](arts/benchmark_en_01.png)

> Die Benchmarks wurden auf einem Apple MacBook Pro mit M5-Chip durchgeführt. Auf Hardware mit niedrigeren Spezifikationen ist der Leistungsvorteil von Reqable noch deutlicher.

# Mobile App

Die mobile Edition bietet Funktionsparität mit der Desktop-Version und ermöglicht sowohl API-Debugging als auch API-Tests für unterwegs. Sie unterstützt das Hinzufügen eines Desktop-Geräts per QR-Code-Scan, sodass mobiler Traffic zur tiefergehenden Inspektion und Bearbeitung an den Desktop weitergeleitet werden kann.

Mit einer optionalen Kontoanmeldung kann die Cloud-Synchronisation aktiviert werden, um Daten automatisch über alle verbundenen Geräte hinweg zu replizieren.

![](arts/screenshot_en_04.png)

> Haltepunkte, Rewriting und Scripting-Funktionen sind aufgrund plattformspezifischer Sicherheitsrichtlinien derzeit auf mobilen Plattformen nicht verfügbar.

# Installation

| Plattform | Architektur | Format | Download & Installation | Hinweise |
| ---- | ---- | ---- | ---- | ---- |
| **Windows** | x86_64 | exe | [Download](https://app.reqable.com/download?platform=windows&arch=x86_64&ext=exe&locale=en-US) | Installer-Version (empfohlen), unterstützt `Windows 7+`. |
| **Windows** | x86_64 | zip | [Download](https://app.reqable.com/download?platform=windows&arch=x86_64&ext=zip&locale=en-US) | Portable-Version, unterstützt `Windows 7+`. |
| **Mac** | universal | - | brew install reqable | Erfordert macOS `11.0` oder neuer. |
| **Mac** | Intel Chip | dmg | [Download](https://app.reqable.com/download?platform=macos&arch=x86_64&ext=dmg&locale=en-US) | Intel-Chip, erfordert macOS `11.0` oder neuer. |
| **Mac** | Apple Silicon | dmg | [Download](https://app.reqable.com/download?platform=macos&arch=arm64&ext=dmg&locale=en-US) | M-Serie-Chip, erfordert macOS `11.0` oder neuer. |
| **Linux** | x86_64 | deb | [Download](https://app.reqable.com/download?platform=linux&arch=x86_64&ext=deb&locale=en-US) | Unterstützt `Ubuntu`, `Debian` und andere Distributionen. Erfordert `GTK 3.0`. |
| **Linux** | x86_64 | AppImage | [Download](https://app.reqable.com/download?platform=linux&arch=x86_64&ext=AppImage&locale=en-US) | Unterstützt `Ubuntu`, `Debian` und andere Distributionen. Erfordert `GTK 3.0`. |
| **Android** | universal | - | [Google Play](https://play.google.com/store/apps/details?id=com.reqable.android) | Erfordert `Android 5.0` oder neuer. |
| **Android** | arm64-v8a | apk | [Download](https://app.reqable.com/download?platform=android&arch=arm64&ext=apk&locale=en-US) | Erfordert `Android 5.0` oder neuer. |
| **Android** | armeabi-v7a | apk | [Download](https://app.reqable.com/download?platform=android&arch=arm&ext=apk&locale=en-US) | Erfordert `Android 5.0` oder neuer. |
| **Android** | x86_64 | apk | [Download](https://app.reqable.com/download?platform=android&arch=x86_64&ext=apk&locale=en-US) | Erfordert `Android 5.0` oder neuer. |
| **iOS** | arm64 | - | [App Store](https://apps.apple.com/cn/app/id6473166828) | Erfordert `iOS 13.0` oder neuer. |

## Dokumentation
https://reqable.com/en-US/docs/introduction

## Danksagungen

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
