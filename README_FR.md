# Reqable

[English](README.md) | [简体中文](README_CN.md) | [繁體中文](README_ZH-HANT.md) | [日本語](README_JA.md) | [한국어](README_KO.md) | [Español](README_ES.md) | [Français](README_FR.md) | [Deutsch](README_DE.md) | [Русский](README_RU.md)

⚠️ **Remarque : Reqable n'est pas un projet open source. Ce dépôt est utilisé exclusivement pour le suivi des problèmes, les demandes de fonctionnalités et les retours des utilisateurs.**

## À propos

[Reqable](https://reqable.com/) est une plateforme de débogage et de test d'API tout-en-un de nouvelle génération. Elle offre une prise en charge multiplateforme, une architecture sans connexion obligatoire, une empreinte légère, un haut débit et une expérience sans publicité — le tout conçu pour simplifier les flux de travail API des développeurs et des ingénieurs QA. Reqable prend en charge cinq plateformes majeures : `Windows`, `macOS`, `Linux`, `Android` et `iOS`.

Reqable combine un outil de capture de trafic API avec un client de test API complet dans un environnement unique et profondément intégré, permettant des flux de travail fluides de capture et de test, et remplaçant plusieurs outils autonomes.

![](arts/products_en.png)

La majorité des fonctionnalités de Reqable sont disponibles gratuitement, sans période d'essai. L'édition Community couvre les besoins de la plupart des développeurs individuels ; les utilisateurs avancés et les équipes peuvent bénéficier d'une mise à niveau vers le niveau Premium pour des fonctionnalités avancées.

Visitez notre site officiel : https://reqable.com

## Sommaire

- [À propos](#à-propos)
- [Débogage d'API](#débogage-dapi)
- [Test d'API](#test-dapi)
- [Support MCP](#support-mcp)
- [Performance extrême](#performance-extrême)
- [Application mobile](#application-mobile)
- [Installation](#installation)
- [Documentation](#documentation)
- [Remerciements](#remerciements)

# Débogage d'API

Reqable utilise une stratégie MITM (Man-in-the-Middle) classique pour intercepter le trafic HTTP(S). Sur les plateformes de bureau, elle capture le trafic via la configuration du proxy au niveau du système ; sur mobile, elle utilise un VPN local. Le trafic capturé peut être inspecté et manipulé grâce à un riche ensemble de primitives de débogage : relecture de requêtes, édition en ligne, points d'arrêt, réécriture d'URL, scripts personnalisés, et plus encore.

![](arts/screenshot_en_01.png)

# Test d'API

Reqable fournit un client API complet pour composer, envoyer et organiser les requêtes `HTTP`, `WebSocket`, `SSE` et `gRPC` (bientôt disponible). Il inclut des collections d'API organisées en dossiers, des variables d'environnement avec résolution par portée, la création intégrée de documentation d'API et la synchronisation cloud entre appareils.

![](arts/screenshot_en_02.png)

# Support MCP

Reqable intègre un serveur MCP (Model Context Protocol) natif, permettant aux assistants IA tels que Claude et GitHub Copilot d'interagir directement avec Reqable. Cela débloque des flux de travail pilotés par l'IA pour le débogage d'API, l'inspection du trafic, la création de règles et les tests automatisés.

![](arts/screenshot_en_03.png)

L'implémentation du serveur MCP est entièrement open source. Consultez le [dépôt MCP Server](https://github.com/reqable/reqable-mcp-server) pour plus de détails.

# Performance extrême

Reqable est conçu avec Flutter et C++, en évitant délibérément un environnement d'exécution de navigateur intégré. Ce choix architectural renforce la sécurité en réduisant la surface d'attaque tout en offrant des gains de performance substantiels par rapport aux alternatives basées sur Electron.

- Temps de démarrage à froid de l'ordre de la milliseconde.
- Empreinte d'installation inférieure à 100 Mo.
- Consommation mémoire typique inférieure à 300 Mo en utilisation active.

Benchmarks de performance de capture de paquets

![](arts/benchmark_en_02.png)

Benchmarks de performance du client API

![](arts/benchmark_en_01.png)

> Les benchmarks ont été réalisés sur un Apple MacBook Pro équipé de la puce M5. Sur du matériel moins performant, l'avantage de Reqable est encore plus marqué.

# Application mobile

L'édition mobile maintient la parité fonctionnelle avec la version de bureau, offrant des capacités de débogage et de test d'API en déplacement. Elle permet d'ajouter un poste de bureau via la lecture d'un code QR, ce qui permet de transférer le trafic mobile vers le bureau pour une inspection et une manipulation approfondies.

Avec une connexion facultative au compte, la synchronisation cloud peut être activée pour répliquer automatiquement les données sur tous les appareils connectés.

![](arts/screenshot_en_04.png)

> Les fonctionnalités de points d'arrêt, de réécriture et de scripting ne sont actuellement pas disponibles sur les plateformes mobiles en raison des politiques de sécurité au niveau de la plateforme.

# Installation

| Plateforme | Architecture | Format | Téléchargement et installation | Remarques |
| ---- | ---- | ---- | ---- | ---- |
| **Windows** | x86_64 | exe | [Télécharger](https://app.reqable.com/download?platform=windows&arch=x86_64&ext=exe&locale=en-US) | Version installateur (recommandée), compatible `Windows 7+`. |
| **Windows** | x86_64 | zip | [Télécharger](https://app.reqable.com/download?platform=windows&arch=x86_64&ext=zip&locale=en-US) | Version portable, compatible `Windows 7+`. |
| **Mac** | universal | - | brew install reqable | Nécessite macOS `11.0` ou ultérieur. |
| **Mac** | Intel Chip | dmg | [Télécharger](https://app.reqable.com/download?platform=macos&arch=x86_64&ext=dmg&locale=en-US) | Puce Intel, nécessite macOS `11.0` ou ultérieur. |
| **Mac** | Apple Silicon | dmg | [Télécharger](https://app.reqable.com/download?platform=macos&arch=arm64&ext=dmg&locale=en-US) | Puce série M, nécessite macOS `11.0` ou ultérieur. |
| **Linux** | x86_64 | deb | [Télécharger](https://app.reqable.com/download?platform=linux&arch=x86_64&ext=deb&locale=en-US) | Compatible `Ubuntu`, `Debian` et autres distributions. Nécessite `GTK 3.0`. |
| **Linux** | x86_64 | AppImage | [Télécharger](https://app.reqable.com/download?platform=linux&arch=x86_64&ext=AppImage&locale=en-US) | Compatible `Ubuntu`, `Debian` et autres distributions. Nécessite `GTK 3.0`. |
| **Android** | universal | - | [Google Play](https://play.google.com/store/apps/details?id=com.reqable.android) | Nécessite `Android 5.0` ou ultérieur. |
| **Android** | arm64-v8a | apk | [Télécharger](https://app.reqable.com/download?platform=android&arch=arm64&ext=apk&locale=en-US) | Nécessite `Android 5.0` ou ultérieur. |
| **Android** | armeabi-v7a | apk | [Télécharger](https://app.reqable.com/download?platform=android&arch=arm&ext=apk&locale=en-US) | Nécessite `Android 5.0` ou ultérieur. |
| **Android** | x86_64 | apk | [Télécharger](https://app.reqable.com/download?platform=android&arch=x86_64&ext=apk&locale=en-US) | Nécessite `Android 5.0` ou ultérieur. |
| **iOS** | arm64 | - | [App Store](https://apps.apple.com/cn/app/id6473166828) | Nécessite `iOS 13.0` ou ultérieur. |

## Documentation
https://reqable.com/en-US/docs/introduction

## Remerciements

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
