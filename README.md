<h1 align="center">¡Hola! Soy Isaac </h1>
<h3 align="center">Actualmente estudiando | ESIME, IPN</h3>

<p align="center">
  Construyo sistemas donde el hardware y el software se encuentran: robots, telemetría en tiempo real, HMIs distribuidos y lo que se me vaya ocurriendo.
</p>

---

### Sobre mí

- Estudiante de Ingeniería en Electrónica y Comunicaciones — ESIME Zacatenco, IPN.
- Me obsesiona la integración hardware-software: firmware, visión, control en tiempo real.
- Python para todo lo que no es firmware: scripting, automatización, bots, etc.
- Actualmente construyendo un sistema HMI distribuido (ESP32 + WebSocket + telemetría de Spotify).
- Aprendiendo a llevar cada proyecto a nivel "portafolio": pruebas unitarias, arquitectura modular, documentación real.
- Me gusta mucho Chiikawa.

---

###  Proyectos destacados

<br>

#### [Robotic Pet — Pan-Tilt Vision System](https://github.com/chac7127/robotic-pet)
![Status](https://img.shields.io/badge/status-en%20desarrollo%20activo-yellow?style=flat-square)

Sistema embebido de visión artificial sobre un Seeed XIAO ESP32S3 Sense. Arquitectura modular diseñada para optimizar latencia separando tareas por núcleo:

- **Core 1:** Procesamiento de visión y detección de movimiento.
- **Core 0:** Control de servomotores suavizado a 50 Hz mediante FreeRTOS.
- **Interacción:** Capa de voz delegada a servidor externo usando Whisper, Ollama y Piper TTS.
- **Calidad de código:** Respaldado por [29 pruebas unitarias](https://github.com/TU_USUARIO/robotic-pet/tree/main/test) utilizando Unity sobre entorno nativo de PlatformIO.

`C++17` `PlatformIO` `FreeRTOS` `Computer Vision` `Unity Testing`

<br>

---

<br>

#### [Algorithmic Paper Trading Bot](https://github.com/chac7127/trading-bot)
![Status](https://img.shields.io/badge/status-en%20producci%C3%B3n-brightgreen?style=flat-square)


Bot de trading algorítmico con estrategia híbrida sobre 4 tickers + un ETF de refugio, desplegado de forma autónoma vía GitHub Actions:

- **Estrategia:** Combina indicadores técnicos (ADX, RSI, Bollinger Bands) con análisis de sentimiento vía FinBERT.
- **Persistencia:** Estado guardado en JSON, con la propia automatización haciendo commit de sus resultados al repo.
- **Infraestructura:** Migrado de Task Scheduler local a GitHub Actions, con cron-job.org como dispatcher externo.
- **Observabilidad:** Notificaciones en tiempo real vía Telegram y caché de datos históricos en formato Parquet.

`Python` `Alpaca API` `FinBERT` `GitHub Actions`

<br>

---

<br>

#### [Distributed HMI System — ESP32 + Spotify](https://github.com/chac7127/hmi-spotify)
![Status](https://img.shields.io/badge/status-en%20desarrollo%20activo-yellow?style=flat-square)

Sistema de interfaz distribuida que convierte un Galaxy S4 en pantalla secundaria conectada por WebSocket, mostrando telemetría de Spotify en tiempo real:

- **Puente Python:** Conexión persistente por WebSocket (migrada de polling) que consulta la API de Spotify y transmite estado + carátula del álbum.
- **Firmware ESP32:** Mensajería estructurada en JSON usando ArduinoJson v7.
- **Compatibilidad:** UI rediseñada con layouts basados en `float` y prefijos de vendor para funcionar dentro de las limitaciones de Chromium ~37-40 del dispositivo.

`ESP32` `WebSockets` `ArduinoJson` `Python`

<br>

---

<br>

#### [Real-Time Hand Tracking](https://github.com/chac7127/hand-tracking)
![Status](https://img.shields.io/badge/status-terminado-blue?style=flat-square)

Clasificador de gestos en tiempo real construido sobre OpenCV y MediaPipe:

- **Gestos soportados:** pointing, peace, thumbs_up, open_palm, fist.
- **Método:** Heurísticas geométricas sobre landmarks de mano, con filtro de media móvil para estabilizar la detección.
- **Robustez:** Resuelto un breaking change en la API de MediaPipe fijando la versión a 0.10.21.

`Python` `OpenCV` `MediaPipe`

---

### Stack técnico

<p align="left">
  <img src="https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/ESP32-E7352C?style=for-the-badge&logo=espressif&logoColor=white" />
  <img src="https://img.shields.io/badge/PlatformIO-FF7F00?style=for-the-badge&logo=platformio&logoColor=white" />
  <img src="https://img.shields.io/badge/FreeRTOS-000000?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" />
</p>

---

### GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=chac7127&show_icons=true&theme=radical" width="48%" />
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=chac7127&theme=radical" width="48%" />
</p>

---

### Contacto

<p align="left">
  <a href="https://www.linkedin.com/in/isaac-emmauel-garc%C3%ADa-angeles-ice/" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
