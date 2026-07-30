# Reqable

[English](README.md) | [简体中文](README_CN.md) | [繁體中文](README_ZH-HANT.md) | [日本語](README_JA.md) | [한국어](README_KO.md) | [Español](README_ES.md) | [Français](README_FR.md) | [Deutsch](README_DE.md) | [Русский](README_RU.md)

⚠️ **Примечание: Reqable не является проектом с открытым исходным кодом. Этот репозиторий используется исключительно для отслеживания проблем, запросов функций и обратной связи от пользователей.**

## О продукте

[Reqable](https://reqable.com/) — это универсальная платформа нового поколения для отладки и тестирования API. Она предлагает кроссплатформенную поддержку, архитектуру без обязательного входа в систему, минимальное потребление ресурсов, высокую пропускную способность и отсутствие рекламы — всё это создано для оптимизации рабочих процессов API у разработчиков и QA-инженеров. Reqable поддерживает пять основных платформ: `Windows`, `macOS`, `Linux`, `Android` и `iOS`.

Reqable объединяет инструмент захвата трафика API с полнофункциональным клиентом для тестирования API в единой, глубоко интегрированной среде, обеспечивая бесшовные рабочие процессы захвата и тестирования и заменяя множество отдельных инструментов.

![](arts/products_en.png)

Большинство функций Reqable доступны бесплатно, без пробного периода. Community-версия покрывает потребности большинства индивидуальных разработчиков; опытные пользователи и команды могут перейти на Premium-уровень для получения расширенных возможностей.

Посетите наш официальный сайт: https://reqable.com

## Содержание

- [О продукте](#о-продукте)
- [Отладка API](#отладка-api)
- [Тестирование API](#тестирование-api)
- [Поддержка MCP](#поддержка-mcp)
- [Экстремальная производительность](#экстремальная-производительность)
- [Мобильное приложение](#мобильное-приложение)
- [Установка](#установка)
- [Документация](#документация)
- [Благодарности](#благодарности)

# Отладка API

Reqable использует классическую стратегию MITM (Man-in-the-Middle) для перехвата HTTP(S)-трафика. На настольных платформах трафик захватывается через системную конфигурацию прокси; на мобильных устройствах используется локальный VPN. Захваченный трафик можно проверять и изменять с помощью богатого набора отладочных примитивов: повтор запросов, встроенное редактирование, точки останова, перезапись URL, пользовательские сценарии и многое другое.

![](arts/screenshot_en_01.png)

# Тестирование API

Reqable предоставляет полнофункциональный API-клиент для составления, отправки и организации запросов `HTTP`, `WebSocket`, `SSE` и `gRPC` (в ближайшее время). Он включает коллекции API с организацией по папкам, переменные окружения с разрешением по области видимости, встроенное создание документации API и облачную синхронизацию между устройствами.

![](arts/screenshot_en_02.png)

# Поддержка MCP

Reqable оснащён встроенным MCP-сервером (Model Context Protocol), позволяющим ИИ-ассистентам, таким как Claude и GitHub Copilot, напрямую взаимодействовать с Reqable. Это открывает возможности для ИИ-управляемых рабочих процессов по отладке API, инспекции трафика, созданию правил и автоматизированному тестированию.

![](arts/screenshot_en_03.png)

Реализация MCP-сервера имеет открытый исходный код. Подробнее см. в [репозитории MCP Server](https://github.com/reqable/reqable-mcp-server).

# Экстремальная производительность

Reqable разработан на Flutter и C++, намеренно избегая встроенной браузерной среды выполнения. Этот архитектурный выбор повышает безопасность за счёт уменьшения поверхности атаки, одновременно обеспечивая значительные преимущества в производительности по сравнению с альтернативами на базе Electron.

- Время холодного запуска на уровне миллисекунд.
- Установочный размер менее 100 МБ.
- Типичное потребление памяти менее 300 МБ при активном использовании.

Тесты производительности захвата пакетов

![](arts/benchmark_en_02.png)

Тесты производительности API-клиента

![](arts/benchmark_en_01.png)

> Тесты проводились на Apple MacBook Pro с чипом M5. На оборудовании с более низкими характеристиками преимущество Reqable в производительности ещё более заметно.

# Мобильное приложение

Мобильная версия сохраняет паритет функций с настольной, предлагая возможности отладки и тестирования API в пути. Поддерживается добавление настольного устройства через сканирование QR-кода, что позволяет перенаправлять мобильный трафик на компьютер для углублённой инспекции и манипуляции.

При входе в учётную запись можно включить облачную синхронизацию для автоматической репликации данных между всеми подключёнными устройствами.

![](arts/screenshot_en_04.png)

> Функции точек останова, перезаписи и сценариев в настоящее время недоступны на мобильных платформах из-за политик безопасности на уровне платформы.

# Установка

| Платформа | Архитектура | Формат | Загрузка и установка | Примечания |
| ---- | ---- | ---- | ---- | ---- |
| **Windows** | x86_64 | exe | [Скачать](https://app.reqable.com/download?platform=windows&arch=x86_64&ext=exe&locale=en-US) | Версия с установщиком (рекомендуется), поддерживается `Windows 7+`. |
| **Windows** | x86_64 | zip | [Скачать](https://app.reqable.com/download?platform=windows&arch=x86_64&ext=zip&locale=en-US) | Портативная версия, поддерживается `Windows 7+`. |
| **Mac** | universal | - | brew install reqable | Требуется macOS `11.0` или новее. |
| **Mac** | Intel Chip | dmg | [Скачать](https://app.reqable.com/download?platform=macos&arch=x86_64&ext=dmg&locale=en-US) | Чип Intel, требуется macOS `11.0` или новее. |
| **Mac** | Apple Silicon | dmg | [Скачать](https://app.reqable.com/download?platform=macos&arch=arm64&ext=dmg&locale=en-US) | Чип серии M, требуется macOS `11.0` или новее. |
| **Linux** | x86_64 | deb | [Скачать](https://app.reqable.com/download?platform=linux&arch=x86_64&ext=deb&locale=en-US) | Поддерживаются `Ubuntu`, `Debian` и другие дистрибутивы. Требуется `GTK 3.0`. |
| **Linux** | x86_64 | AppImage | [Скачать](https://app.reqable.com/download?platform=linux&arch=x86_64&ext=AppImage&locale=en-US) | Поддерживаются `Ubuntu`, `Debian` и другие дистрибутивы. Требуется `GTK 3.0`. |
| **Android** | universal | - | [Google Play](https://play.google.com/store/apps/details?id=com.reqable.android) | Требуется `Android 5.0` или новее. |
| **Android** | arm64-v8a | apk | [Скачать](https://app.reqable.com/download?platform=android&arch=arm64&ext=apk&locale=en-US) | Требуется `Android 5.0` или новее. |
| **Android** | armeabi-v7a | apk | [Скачать](https://app.reqable.com/download?platform=android&arch=arm&ext=apk&locale=en-US) | Требуется `Android 5.0` или новее. |
| **Android** | x86_64 | apk | [Скачать](https://app.reqable.com/download?platform=android&arch=x86_64&ext=apk&locale=en-US) | Требуется `Android 5.0` или новее. |
| **iOS** | arm64 | - | [App Store](https://apps.apple.com/cn/app/id6473166828) | Требуется `iOS 13.0` или новее. |

## Документация
https://reqable.com/en-US/docs/introduction

## Благодарности

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
