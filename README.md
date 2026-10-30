<h1 align="center">¡Hola! Soy Isaac</h1>
<h3 align="center">Ingeniería en Comunicaciones y Electrónica | ESIME Zacatenco, IPN</h3>

<p align="center">
  Construyo sistemas donde el hardware y el software se encuentran: robots, telemetría en tiempo real, HMIs distribuidos y lo que se me vaya ocurriendo.
</p>

---

### Sobre mí

- Estudio Ingeniería en Comunicaciones y Electrónica en la ESIME Zacatenco, IPN.
- Me apasiona la integración hardware-software: diseño desde el firmware y el acondicionamiento de sensores hasta la visión artificial y el control en tiempo real.
- Utilizo Python para todo lo que vive fuera del microcontrolador: scripting, automatización, pipelines de datos y bots.
- Dándole vida actualmente a **Hachiware**, una mascota virtual física donde combino diseño electrónico, máquinas de estados y animaciones en bajo nivel.
- Llevo cada proyecto a nivel portafolio aplicando pruebas unitarias, arquitectura modular y documentación real.

---

### Proyectos destacados

<br>

#### [Hachiware — Interactive Companion Pet](https://github.com/chac7127/hachiware)
![Status](https://img.shields.io/badge/status-en%20desarrollo%20activo-yellow?style=flat-square)

Mascota virtual de escritorio construida desde cero sobre un ESP32, donde una arquitectura modular en C++ da vida al personaje separando por completo los drivers físicos de su comportamiento:

- **Lógica de comportamiento:** Gobierna las reacciones del personaje mediante una máquina de estados finita (FSM) no bloqueante (`millis()`), centralizando parámetros y umbrales en `config.h` como única fuente de verdad.
- **Interacción física:** Captura toques y pequeños golpes a través de un sensor piezoeléctrico, acondicionando la señal para distinguir caricias o llamados reales frente a la vibración de la mesa.
- **Expresión visual:** Renderiza animaciones y estados de ánimo en una pantalla OLED de 1.3" (I2C), alojando los *sprites* en memoria Flash (`PROGMEM`) para mantener libre la SRAM del microcontrolador.
- **Respuesta auditiva:** Acompaña cada cambio de humor con secuencias acústicas asíncronas que refuerzan la personalidad del sistema sin detener el bucle principal.

`C++` `ESP32` `PlatformIO` `FSM` `Embedded Systems`

<br>

---

<br>

#### [Robotic Pet — Pan-Tilt Vision System](https://github.com/chac7127/robotic-pet)
![Status](https://img.shields.io/badge/status-en%20desarrollo%20activo-yellow?style=flat-square)

Sistema embebido de visión artificial sobre un Seeed XIAO ESP32-S3 Sense, estructurado bajo una arquitectura modular que optimiza la latencia repartiendo la carga entre ambos núcleos:

- **Procesamiento visual (Core 1):** Ejecuta la captura de cámara y detección de movimiento de forma dedicada para evitar caídas de *frames*.
- **Control de movimiento (Core 0):** Gestiona el lazo de control de los servomotores suavizado a 50 Hz mediante tareas de FreeRTOS.
- **Interacción por voz:** Delega el procesamiento conversacional a un servidor externo integrando Whisper, Ollama y Piper TTS.
- **Calidad de código:** Valida la lógica de control y estado mediante [29 pruebas unitarias](https://github.com/chac7127/robotic-pet/tree/main/test) con Unity en el entorno nativo de PlatformIO.

`C++17` `PlatformIO` `FreeRTOS` `Computer Vision` `Unity Testing`

<br>

---

<br>

#### [Algorithmic Paper Trading Bot](https://github.com/chac7127/trading-bot)
![Status](https://img.shields.io/badge/status-en%20producci%C3%B3n-brightgreen?style=flat-square)

Bot de trading algorítmico que opera una estrategia híbrida sobre 4 tickers y un ETF de refugio, ejecutándose de manera autónoma en la nube mediante GitHub Actions:

- **Estrategia de decisión:** Combina indicadores técnicos clásicos (ADX, RSI, Bandas de Bollinger) con análisis de sentimiento financiero procesado con FinBERT.
- **Persistencia de estado:** Registra la cartera y las operaciones en JSON, haciendo *commit* automático de sus propios resultados directamente al repositorio tras cada ejecución.
- **Infraestructura autónoma:** Opera sobre flujos de GitHub Actions (migrado desde Task Scheduler local), utilizando cron-job.org como *dispatcher* externo para asegurar la puntualidad del mercado.
- **Observabilidad y datos:** Envía reportes de ejecución en tiempo real vía Telegram y acelera las consultas almacenando el histórico de precios en formato Parquet.

`Python` `Alpaca API` `FinBERT` `GitHub Actions`

<br>

---

<br>

#### [Distributed HMI System — ESP32 + Spotify](https://github.com/chac7127/hmi-spotify)
![Status](https://img.shields.io/badge/status-en%20desarrollo%20activo-yellow?style=flat-square)

Sistema de interfaz distribuida que recicla un Samsung Galaxy S4 como pantalla secundaria dedicada, sincronizando telemetría de Spotify en tiempo real a través de WebSockets:

- **Puente de datos:** Mantiene una conexión persistente en Python (migrada de *polling* a WebSockets) que consulta la API de Spotify y transmite metadatos junto con la carátula del álbum.
- **Enrutamiento en firmware:** Procesa y despacha la mensajería estructurada desde el ESP32 utilizando ArduinoJson v7.
- **Adaptación retro-web:** Rediseña la interfaz gráfica con *layouts* basados en `float` y prefijos de *vendor* específicos para sortear las limitaciones del motor Chromium (~37-40) nativo del teléfono.

`ESP32` `WebSockets` `ArduinoJson` `Python`

<br>

---

<br>

#### [Real-Time Hand Tracking](https://github.com/chac7127/hand-tracking)
![Status](https://img.shields.io/badge/status-terminado-blue?style=flat-square)

Clasificador de gestos manuales en tiempo real construido en Python sobre OpenCV y MediaPipe para interfaces sin contacto:

- **Reconocimiento:** Identifica cinco poses distintas (*pointing*, *peace*, *thumbs_up*, *open_palm* y *fist*) en transmisión de video continua.
- **Estabilidad geométrica:** Evalúa heurísticas vectoriales sobre los *landmarks* de la mano y aplica un filtro de media móvil que elimina el parpadeo entre transiciones.
- **Control de dependencias:** Garantiza la reproducibilidad del entorno fijando MediaPipe en la versión `0.10.21` tras resolver un *breaking change* en la API de dibujo.

`Python` `OpenCV` `MediaPipe`

<br>

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
  <a href="https://www.linkedin.com/in/isaac-emmauel-garc%C3%ADa-angeles-ice/" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
</p>
