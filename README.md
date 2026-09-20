# HOMEBD

**HOMEBD — Home Assistant Onboard Monitoring & Board Data**

Independent Android application for read-only OBD-II vehicle monitoring and diagnostics, with optional Home Assistant integration.

**Current release: Beta 1.0.0**

## Features

- Bluetooth OBD-II adapter connection
- OBD-II / CAN diagnostic communication
- Read-only vehicle monitoring and diagnostics
- Automatic diagnostic parameter discovery
- VIN discovery where supported
- LIVE DATA
- Optional Home Assistant integration
- Real-time HOMEBD telemetry
- `sensor.homebd_*` entity namespace

## Language

HOMEBD detects the Android system language automatically. When a supported language is available, it is selected automatically. English is used as the fallback language.

## Installation

See [INSTALLATION_GUIDE.md](INSTALLATION_GUIDE.md).

## Home Assistant

Home Assistant integration is optional.

See [INSTALLATION_GUIDE.md](INSTALLATION_GUIDE.md) for setup information.

## Project documentation

- [ABOUT.md](ABOUT.md)
- [INSTALLATION_GUIDE.md](INSTALLATION_GUIDE.md)
- [LICENSES.md](LICENSES.md)
- [LICENSE](LICENSE)

## License

Original HOMEBD source code and documentation are released under the MIT License unless otherwise stated.

The HOMEBD name, logo, icons and original graphics are original project assets created for HOMEBD and owned by lufime. The MIT software licence does not grant trademark rights to the official HOMEBD visual identity.

See [LICENSES.md](LICENSES.md) for external component licences and official licence links.

## Beta status

HOMEBD Beta 1.0.0 is a development release. Diagnostic coverage, supported parameters, interface elements and integration behaviour may change in future releases.
