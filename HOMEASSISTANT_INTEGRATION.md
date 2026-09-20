# HOMEBD — Home Assistant Integration

**Release:** Beta 1.0.0.0

## Overview

HOMEBD provides an optional Home Assistant integration for publishing vehicle telemetry collected by the Android application.

The integration is dedicated to HOMEBD and does not require unrelated vehicle applications or external diagnostic databases.

## Architecture

```text
Vehicle
  ↓
Diagnostic adapter
  ↓
HOMEBD Android
  ↓
Home Assistant connection
  ↓
HOMEBD integration
  ↓
sensor.homebd_*
```

## Installation

Place the HOMEBD integration in:

`/config/custom_components/homebd/`

Restart Home Assistant and open:

**Settings → Devices & services → Add Integration → HOMEBD**

## Android configuration

In the HOME ASSISTANT section of HOMEBD configure:

- Home Assistant address
- Home Assistant access token

The application establishes the Home Assistant connection and authenticates using the configured credentials.

## Entities

HOMEBD telemetry uses the entity namespace:

`sensor.homebd_*`

Only HOMEBD telemetry is intended to be handled by this integration.

## Real-time operation

The integration is designed for real-time publication of HOMEBD readings. Sensor availability depends on the Android application, vehicle connection, diagnostic adapter and network connection.

## Security

- Protect Home Assistant access tokens.
- Use secure network connections where appropriate.
- Vehicle communication remains read-only.
- HOMEBD does not intentionally perform vehicle programming, coding or ECU reset operations.

## Licensing

The HOMEBD integration is part of the HOMEBD project and is covered by the project licence unless a file explicitly states otherwise.

See [LICENSE](LICENSE) and [LICENSES.md](LICENSES.md).
