# PollingRateTester

A macOS mouse polling-rate tester with live IPS measurement and multiple input backends.

## Features
- Mouse polling-rate measurement and statistical analysis
- Live mouse speed estimation (IPS)
- Configurable CPI
- Four input modes: Native HID, Direct HID, CGEventTap, and AppKit
- Universal support for Apple Silicon and Intel Macs

## Input Methods

| Mode | Description |
|---|---|
| **Native HID** | Device-targeted HID input monitoring. |
| **Direct HID** | HID element-based input monitoring using IOHIDManager. |
| **CGEventTap** | Monitors mouse events through the macOS Quartz event system. |
| **AppKit** | Measures mouse events delivered to the application. |

HID-based modes can provide more device-oriented input data, while CGEventTap and AppKit observe events at higher system or application layers. Actual accuracy depends on the implementation and macOS event delivery.

**Note:** Observed event rate does not necessarily equal the mouse's verified hardware polling rate. IPS is an estimate whose accuracy depends on the available movement data and CPI calibration.

every online polling rate browser base tester use appkit and its not accurate 
Most accurate one is the native HID

## Download

Download the latest version from [GitHub Releases](https://github.com/HIRBOWD/PollingRateTester/releases).

- **DMG:** Recommended for most users.
- **ZIP:** Portable application bundle.
- **CLI:** Command-line version.

## Installation

1. Download the DMG.
2. Open it.
3. Drag `PollingRateTester.app` into Applications.
4. Launch the application.

The initial release may not be notarized by Apple, so macOS may display a security warning.

## License

Specify a license before granting permission to reuse or redistribute the source code.
