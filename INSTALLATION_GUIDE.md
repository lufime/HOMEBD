# HOMEBD — Beta 1.0.0.0 Installation Guide

## 1. About this release

This guide applies specifically to **HOMEBD Beta 1.0.0.0**.

HOMEBD is intended for read-only vehicle monitoring and diagnostics. It must not be used for vehicle programming, coding, configuration changes or ECU resets.

## 2. Requirements

Prepare:

- A compatible Android device.
- A compatible Bluetooth OBD-II adapter.
- A vehicle with an accessible diagnostic connector.
- Home Assistant, only if the optional integration is required.

Supported vehicle data depends on the vehicle, control units, adapter and available diagnostic responses.

## 3. Install the Android application

1. Obtain the HOMEBD Beta 1.0.0.0 APK from the project release.
2. Install the APK on the Android device.
3. Grant the Android permissions requested by HOMEBD.
4. Open HOMEBD.
5. Keep Bluetooth enabled.

## 4. Prepare the vehicle connection

1. Switch the vehicle to the required ignition state.
2. Connect the compatible diagnostic adapter to the vehicle.
3. Wait for the adapter to become available.
4. Pair the adapter with Android when pairing is required.
5. Return to HOMEBD.

## 5. Connect HOMEBD

1. Open the Bluetooth/device section.
2. Select the available diagnostic adapter.
3. Press **Connect**.
4. Wait for initialization to finish.
5. Confirm that the application reports a valid connection.

Do not repeatedly start new connection or scan operations while initialization is in progress.

## 6. Diagnostic scan

1. Start the diagnostic scan.
2. HOMEBD identifies supported diagnostic parameters.
3. Available parameters are used by LIVE DATA.
4. Run another scan only when a fresh discovery is required.

The number and type of available parameters vary between vehicles and control units.

## 7. LIVE DATA

1. Open **LIVE DATA**.
2. Start live monitoring.
3. Confirm that supported values are being updated.
4. Keep the diagnostic adapter connected while monitoring.

If communication is interrupted, allow HOMEBD to re-establish the connection before continuing normal monitoring.

## 8. Home Assistant — optional

Home Assistant integration is optional and is not required for local vehicle diagnostics.

To install the integration:

1. Open the Home Assistant configuration directory.
2. Create the directory:
   `custom_components/homebd/`
3. Copy the HOMEBD integration files into that directory.
4. Restart Home Assistant.
5. Open **Settings → Devices & services**.
6. Select **Add Integration**.
7. Search for **HOMEBD**.
8. Complete the configuration.

Only HOMEBD integration files should be placed in the HOMEBD integration directory.

## 9. Configure Home Assistant in HOMEBD

Inside the HOME ASSISTANT section of the Android application:

1. Enter the Home Assistant address.
2. Enter a valid Home Assistant access token.
3. Save the configuration.
4. Start the Home Assistant connection.
5. Confirm that the connection is authenticated.
6. Verify that HOMEBD entities appear in Home Assistant.

The integration is designed to expose HOMEBD telemetry under the `sensor.homebd_*` namespace.

## 10. Security

- Vehicle communication is read-only.
- Do not use HOMEBD while driving unless the application and vehicle setup are specifically designed for safe operation.
- Protect Home Assistant access credentials and tokens.
- Do not share access tokens publicly.

## 11. Troubleshooting

### Adapter not visible
Check Bluetooth, adapter power, pairing and vehicle ignition state.

### Connection fails
Disconnect and reconnect the adapter, then restart the connection process.

### No diagnostic values
Run a fresh scan and verify that the vehicle is in the required ignition state.

### Home Assistant not connecting
Check the Home Assistant address, network connectivity, access token and integration installation.

### Entities unavailable
Restart the Home Assistant integration and verify that the Android application is connected and sending telemetry.

## 12. Beta notice

HOMEBD Beta 1.0.0.0 is a development release. Diagnostic coverage and integration behaviour may vary by vehicle and hardware.
