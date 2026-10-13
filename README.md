<h1 align="center">ESP32 Project Course</h1>
<p align="center"><em>PlatformIO starter project for an ESP32 project course, on the Arduino framework.</em></p>

<p align="center">
  <a href="#overview"><img src="https://img.shields.io/badge/status-starter%20template-6e7781?style=flat-square" alt="Status: starter template"></a>
  <a href="platformio.ini"><img src="https://img.shields.io/badge/board-esp32dev-1f6feb?style=flat-square" alt="Board: esp32dev"></a>
  <a href="platformio.ini"><img src="https://img.shields.io/badge/partition-huge__app-6e7781?style=flat-square" alt="Partition: huge_app"></a>
</p>
<p align="center">
  <img src="https://img.shields.io/badge/ESP32-espressif32-e7352c?style=flat-square&logo=espressif&logoColor=white" alt="ESP32 (espressif32)">
  <img src="https://img.shields.io/badge/PlatformIO-build-f5822a?style=flat-square&logo=platformio&logoColor=white" alt="PlatformIO">
  <img src="https://img.shields.io/badge/Arduino-framework-00878f?style=flat-square&logo=arduino&logoColor=white" alt="Arduino framework">
  <img src="https://img.shields.io/badge/C%2B%2B-firmware-00599c?style=flat-square&logo=cplusplus&logoColor=white" alt="C++">
  <a href="LICENSE"><img src="https://img.shields.io/github/license/jacedeno/esp32-project-course?style=flat-square" alt="License"></a>
  <img src="https://img.shields.io/github/last-commit/jacedeno/esp32-project-course?style=flat-square" alt="Last commit">
</p>

## Overview

Repository for an ESP32 project course. It holds a PlatformIO project for the
`esp32dev` board on the Arduino framework, ready to build and flash: `src/main.cpp`
is still the empty `setup()` / `loop()` skeleton.

## Features

- **Board:** `esp32dev` on the `espressif32` platform, Arduino framework.
- **Partition table:** `huge_app.csv`, for a larger application image.
- **Upload:** `esptool` at 921600 baud. **Serial monitor:** 115200 baud.
- **Libraries staged, not enabled:** `platformio.ini` lists ESPAsyncWebServer,
  ArduinoJson, PubSubClient (MQTT) and Time as commented-out dependencies, to
  switch on as the course needs them.

## Project layout

| Path | Contents |
|---|---|
| [`platformio.ini`](platformio.ini) | Build environment `esp32dev` and the staged library list |
| [`src/main.cpp`](src/main.cpp) | Firmware entry point (`setup()` / `loop()`) |
| `include/`, `lib/`, `test/` | PlatformIO's standard folders for headers, private libraries and unit tests |

## Getting started

1. Install [VS Code](https://code.visualstudio.com/) with the
   [PlatformIO IDE](https://platformio.org/install/ide?install=vscode) extension
   (recommended in `.vscode/extensions.json`), or the PlatformIO Core CLI.
2. Set `upload_port` and `monitor_port` in `platformio.ini` to your board's serial
   port (the file ships with `COM3`).
3. Build, flash and open the serial monitor:

```bash
pio run --target upload
pio device monitor
```

## License

MIT — see [LICENSE](LICENSE).

---

<p align="center">
  Built by <b>Jose Cedeno</b> ·
  <a href="https://geekendzone.com">geekendzone.com</a> ·
  <a href="https://www.linkedin.com/in/joseangelcedeno/">LinkedIn</a>
</p>
