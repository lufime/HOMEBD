# HOMEBD — Home Assistant Integration

**Version: Beta 1.0.1**

## Overview

The HOMEBD Home Assistant integration is optional.

It provides HOMEBD telemetry to Home Assistant through the HOMEBD integration connection.

## Architecture

```text
Vehicle
   ↓
OBD-II adapter
   ↓
HOMEBD Android
   ↓
HOMEBD integration connection
   ↓
Home Assistant
   ↓
sensor.homebd_*
```

## Installation

Install the HOMEBD integration in the Home Assistant configuration according to the integration package included with the project.

The integration files are located in:

```text
/config/custom_components/homebd/
```

Restart Home Assistant after installing or updating the integration.

## Entity namespace

HOMEBD entities use the following namespace:

```text
sensor.homebd_*
```

This keeps HOMEBD entities grouped under a dedicated namespace.

## Operation

When HOMEBD is connected to the vehicle and the Home Assistant integration is active, supported telemetry can be published to Home Assistant.

Unavailable vehicle parameters remain unavailable rather than being replaced with invented values.

## Security

Use appropriate network and Home Assistant authentication controls.

Do not expose Home Assistant credentials or access tokens in screenshots, logs, source files or public repositories.

## Troubleshooting

If HOMEBD entities do not appear:

1. Confirm the integration is installed.
2. Restart Home Assistant.
3. Confirm HOMEBD is connected to the vehicle.
4. Confirm the Android device has network access to Home Assistant.
5. Check Home Assistant logs.
6. Check HOMEBD logs for connection errors.

## Optional feature

Home Assistant integration is optional. HOMEBD can be used independently for local vehicle monitoring and diagnostics.
