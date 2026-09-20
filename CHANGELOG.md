# HOMEBD CHANGELOG

## Beta 1.0.1

Initial documented HOMEBD Beta release.

### Application
- English-mode runtime strings cleaned up to prevent Portuguese UI/log text from appearing when Android is set to English.
- Read-only OBD-II vehicle monitoring and diagnostics.
- Bluetooth OBD-II adapter connection.
- Diagnostic parameter discovery.
- VIN discovery where supported.
- LIVE DATA monitoring.
- Automatic application language detection.
- English fallback when the Android system language is not supported.

### Home Assistant
- Optional Home Assistant integration.
- HOMEBD telemetry support.
- HOMEBD entity namespace: `sensor.homebd_*`.

### Documentation
- Documentation reset at Beta 1.0.1.
- English installation guide.
- Project overview and About documentation.
- Licensing documentation.
- Original HOMEBD icons, logos and graphics documented as project assets.

### Licensing
- Original HOMEBD source code and documentation released under the MIT License.
- External component licences documented separately in `LICENSES.md`.

## Future releases

Changes made after Beta 1.0.1 will be recorded here.


## Build fix
- Fixed an invalid Kotlin string interpolation in `MainActivity.kt` that caused `Unresolved reference: label` during Kotlin compilation.

### Home Assistant telemetry performance
- Added batched `homebd/update_batch` telemetry transport over the persistent WebSocket.
- LIVE DATA now queues the current cycle and sends supported HOMEBD sensor updates in one WebSocket message when the updated integration is installed.
- Added capability detection so older HOMEBD integrations continue to receive individual updates.
