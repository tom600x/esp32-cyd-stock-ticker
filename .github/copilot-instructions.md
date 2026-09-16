# Copilot instructions

## PlatformIO workflow

- This is a PlatformIO project targeting the `esp32dev` environment in
  `platformio.ini` (`ESP32 Dev Module` with the Arduino framework).
- The firmware source is `src/stock_ticker_v3_3.ino`. Keep new firmware source
  files under `src/`; do not restore the sketch to the repository root.
- `User_Setup.h` contains the CYD display configuration. The PlatformIO
  configuration includes it automatically; do not replace it with a generated
  TFT_eSPI setup.
- Build firmware with `pio run` from the repository root. Use `pio run -t
  upload` only when hardware upload is explicitly requested, and
  `pio device monitor` for serial output at 115200 baud.
- Run a clean build with `pio run -t clean` followed by `pio run` when changing
  PlatformIO configuration or dependencies.
- Do not commit generated `.pio/` build output or editor metadata.
- When changing libraries, update `lib_deps` in `platformio.ini` and verify with
  `pio run`.
