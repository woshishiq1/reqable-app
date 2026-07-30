# Reqable

[English](README.md) | [简体中文](README_CN.md) | [繁體中文](README_ZH-HANT.md) | [日本語](README_JA.md) | [한국어](README_KO.md) | [Español](README_ES.md) | [Français](README_FR.md) | [Deutsch](README_DE.md) | [Русский](README_RU.md)

⚠️ **Nota: Reqable no es un proyecto de código abierto. Este repositorio se utiliza exclusivamente para el seguimiento de incidencias, solicitudes de funciones y comentarios de usuarios.**

## Acerca de

[Reqable](https://reqable.com/) es una plataforma integral de depuración y prueba de APIs de nueva generación. Ofrece soporte multiplataforma, una arquitectura sin necesidad de inicio de sesión, una huella ligera, alto rendimiento y una experiencia sin anuncios — todo diseñado para optimizar los flujos de trabajo de API para desarrolladores e ingenieros de QA. Reqable es compatible con cinco plataformas principales: `Windows`, `macOS`, `Linux`, `Android` e `iOS`.

Reqable combina una herramienta de captura de tráfico API con un cliente de prueba de API completo en un único entorno profundamente integrado, permitiendo flujos de trabajo fluidos de captura y prueba, y reemplazando múltiples herramientas independientes.

![](arts/products_en.png)

La mayoría de las funciones de Reqable están disponibles de forma gratuita, sin período de prueba. La edición Community cubre las necesidades de la mayoría de los desarrolladores individuales; los usuarios avanzados y equipos pueden beneficiarse de actualizar al nivel Premium para obtener capacidades avanzadas.

Visite nuestro sitio web oficial: https://reqable.com

## Contenido

- [Acerca de](#acerca-de)
- [Depuración de API](#depuración-de-api)
- [Prueba de API](#prueba-de-api)
- [Soporte MCP](#soporte-mcp)
- [Rendimiento extremo](#rendimiento-extremo)
- [Aplicación móvil](#aplicación-móvil)
- [Instalación](#instalación)
- [Documentación](#documentación)
- [Agradecimientos](#agradecimientos)

# Depuración de API

Reqable emplea una estrategia clásica MITM (Man-in-the-Middle) para interceptar el tráfico HTTP(S). En plataformas de escritorio, captura el tráfico mediante la configuración del proxy a nivel del sistema; en dispositivos móviles, utiliza una VPN local. El tráfico capturado puede inspeccionarse y manipularse mediante un amplio conjunto de primitivas de depuración: repetición de solicitudes, edición en línea, puntos de interrupción, reescritura de URL, scripting personalizado y más.

![](arts/screenshot_en_01.png)

# Prueba de API

Reqable proporciona un cliente API completo para componer, enviar y organizar solicitudes `HTTP`, `WebSocket`, `SSE` y `gRPC` (próximamente). Incluye colecciones de API organizadas por carpetas, variables de entorno con resolución por ámbito, creación integrada de documentación de API y sincronización en la nube entre dispositivos.

![](arts/screenshot_en_02.png)

# Soporte MCP

Reqable incorpora un servidor MCP (Model Context Protocol) integrado, que permite a asistentes de IA como Claude y GitHub Copilot interactuar directamente con Reqable. Esto desbloquea flujos de trabajo impulsados por IA para la depuración de API, inspección de tráfico, creación de reglas y pruebas automatizadas.

![](arts/screenshot_en_03.png)

La implementación del servidor MCP es completamente de código abierto. Consulte el [repositorio MCP Server](https://github.com/reqable/reqable-mcp-server) para más detalles.

# Rendimiento extremo

Reqable está diseñado con Flutter y C++, evitando deliberadamente un entorno de ejecución de navegador integrado. Esta elección arquitectónica refuerza la seguridad al reducir la superficie de ataque, al tiempo que ofrece ganancias de rendimiento sustanciales frente a las alternativas basadas en Electron.

- Tiempo de arranque en frío a nivel de milisegundos.
- Huella de instalación inferior a 100 MB.
- Consumo de memoria típico inferior a 300 MB durante el uso activo.

Pruebas de rendimiento de captura de paquetes

![](arts/benchmark_en_02.png)

Pruebas de rendimiento del cliente API

![](arts/benchmark_en_01.png)

> Las pruebas se realizaron en un Apple MacBook Pro con chip M5. En hardware de especificaciones inferiores, la ventaja de rendimiento de Reqable es aún más pronunciada.

# Aplicación móvil

La edición móvil mantiene la paridad de funciones con la versión de escritorio, ofreciendo capacidades de depuración y prueba de API sobre la marcha. Admite la adición de un equipo de escritorio mediante escaneo de código QR, lo que permite reenviar el tráfico móvil al escritorio para una inspección y manipulación más profundas.

Con un inicio de sesión de cuenta opcional, se puede habilitar la sincronización en la nube para replicar automáticamente los datos en todos los dispositivos conectados.

![](arts/screenshot_en_04.png)

> Las funciones de puntos de interrupción, reescritura y scripting no están disponibles actualmente en plataformas móviles debido a las políticas de seguridad a nivel de plataforma.

# Instalación

| Plataforma | Arquitectura | Formato | Descarga e instalación | Notas |
| ---- | ---- | ---- | ---- | ---- |
| **Windows** | x86_64 | exe | [Descargar](https://app.reqable.com/download?platform=windows&arch=x86_64&ext=exe&locale=en-US) | Versión instalable (recomendada), compatible con `Windows 7+`. |
| **Windows** | x86_64 | zip | [Descargar](https://app.reqable.com/download?platform=windows&arch=x86_64&ext=zip&locale=en-US) | Versión portátil, compatible con `Windows 7+`. |
| **Mac** | universal | - | brew install reqable | Requiere macOS `11.0` o posterior. |
| **Mac** | Intel Chip | dmg | [Descargar](https://app.reqable.com/download?platform=macos&arch=x86_64&ext=dmg&locale=en-US) | Chip Intel, requiere macOS `11.0` o posterior. |
| **Mac** | Apple Silicon | dmg | [Descargar](https://app.reqable.com/download?platform=macos&arch=arm64&ext=dmg&locale=en-US) | Chip serie M, requiere macOS `11.0` o posterior. |
| **Linux** | x86_64 | deb | [Descargar](https://app.reqable.com/download?platform=linux&arch=x86_64&ext=deb&locale=en-US) | Compatible con `Ubuntu`, `Debian` y otras distribuciones. Requiere `GTK 3.0`. |
| **Linux** | x86_64 | AppImage | [Descargar](https://app.reqable.com/download?platform=linux&arch=x86_64&ext=AppImage&locale=en-US) | Compatible con `Ubuntu`, `Debian` y otras distribuciones. Requiere `GTK 3.0`. |
| **Android** | universal | - | [Google Play](https://play.google.com/store/apps/details?id=com.reqable.android) | Requiere `Android 5.0` o posterior. |
| **Android** | arm64-v8a | apk | [Descargar](https://app.reqable.com/download?platform=android&arch=arm64&ext=apk&locale=en-US) | Requiere `Android 5.0` o posterior. |
| **Android** | armeabi-v7a | apk | [Descargar](https://app.reqable.com/download?platform=android&arch=arm&ext=apk&locale=en-US) | Requiere `Android 5.0` o posterior. |
| **Android** | x86_64 | apk | [Descargar](https://app.reqable.com/download?platform=android&arch=x86_64&ext=apk&locale=en-US) | Requiere `Android 5.0` o posterior. |
| **iOS** | arm64 | - | [App Store](https://apps.apple.com/cn/app/id6473166828) | Requiere `iOS 13.0` o posterior. |

## Documentación
https://reqable.com/en-US/docs/introduction

## Agradecimientos

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
