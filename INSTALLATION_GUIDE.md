# HOMEBD — Installation Guide

**Version: Beta 1.0.1**

## 1. Requirements

- Compatible Android device
- Bluetooth enabled
- Compatible Bluetooth OBD-II adapter
- Vehicle with a supported OBD-II diagnostic interface
- Optional Home Assistant installation for remote telemetry

## 2. Install HOMEBD

1. Obtain the HOMEBD Beta 1.0.1 APK from the project release.
2. Install the APK on Android.
3. If Android requests permission to install an APK from the selected source, allow it.
4. Launch **HOMEBD**.

## 3. Connect the OBD-II adapter

1. Turn the vehicle on or switch the ignition to the required diagnostic state.
2. Connect the OBD-II adapter to the vehicle.
3. Enable Bluetooth on Android.
4. Pair the adapter with Android if required.
5. Open HOMEBD.
6. Select the detected adapter.
7. Start the connection.

## 4. Run a diagnostic scan

After connecting:

1. Start the diagnostic scan.
2. Allow HOMEBD to discover available diagnostic parameters.
3. Review the available vehicle data.
4. Open **LIVE DATA** to monitor supported values.

Available parameters depend on the vehicle, diagnostic interface and adapter.

## 5. LIVE DATA

LIVE DATA displays information received from the vehicle through the diagnostic connection.

Unsupported or unavailable values may be shown as unavailable.

HOMEBD is intended for read-only monitoring and diagnostics.

## 6. Home Assistant

Home Assistant integration is optional.

When enabled, HOMEBD can provide supported telemetry to Home Assistant using the HOMEBD integration.

HOMEBD entities use the `sensor.homebd_*` namespace.

## 7. Automatic language detection

HOMEBD reads the Android system language and automatically selects a supported application language.

If the system language is not supported, English is used as the fallback language.

## 8. Troubleshooting

### Adapter not detected
- Confirm Bluetooth is enabled.
- Confirm the adapter is powered.
- Check Android Bluetooth permissions.
- Confirm another application is not already using the adapter.

### Connection fails
- Disconnect and reconnect the adapter.
- Re-pair the adapter if necessary.
- Ensure the vehicle is in the required ignition state.

### Some values are unavailable
Supported diagnostic parameters vary between vehicles and diagnostic interfaces.

### Home Assistant is unavailable
- Confirm the Home Assistant connection settings.
- Confirm the integration is installed correctly.
- Check the Android network connection.
- Review Home Assistant logs.

## 9. Safety

HOMEBD is a monitoring and diagnostic application.

Do not use the application while driving.

Do not perform diagnostic work that could distract the driver.

HOMEBD is designed for read-only operation and does not intentionally perform vehicle programming, coding, ECU flashing or ECU reset operations.

## 10. Beta notice

Beta 1.0.1 is a development release. Features, supported parameters, interface elements and integration behaviour may change in future releases.
