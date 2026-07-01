# DMTool (USB2CANFD)

[中文](./README.md) | [EN](./README.en.md)

This directory only keeps the DMTool V2 host software for USB2CANFD / USB2CANFD-Dual. USB2CAN host software, open protocol files, mechanical files, and usage documents are maintained in the USB2CAN module directory instead of being duplicated here.

USB2CAN materials: `模块/通信模块/USB2CAN`

## Contents

| Platform | File | Description |
| --- | --- | --- |
| Windows x86_64 | `Windows/x86_64/DMTool 2.1.8.1.exe` | Windows executable |
| Linux x86_64 | `Linux/x86_64/DMTool-v2.1.8.1-x86_64.AppImage` | Linux x86_64 AppImage |
| Linux x86_64 | `Linux/x86_64/arch_lib_install.sh` | Arch Linux dependency helper |
| Linux arm64 | `Linux/arm64/DMTool-v2.1.8.1-arm64/start.sh` | Linux arm64 launcher |
| MacOS x86_64 | `MacOS/x86_64/DMTool-v2.1.8.1-x86_64.app.zip` | macOS Intel package |
| MacOS arm64 | `MacOS/arm64/DMTool-v2.1.8.1-arm64.app.zip` | macOS Apple Silicon package |
| Manual | `DMTool上位机软件说明书.pdf` | DMTool user manual |

## Windows

1. Open `Windows/x86_64/`
2. Double-click `DMTool 2.1.8.1.exe`
3. If Windows SmartScreen blocks the app on first launch, choose "More info" and continue

## Linux x86_64

```bash
cd Linux/x86_64
chmod +x DMTool-v2.1.8.1-x86_64.AppImage
./DMTool-v2.1.8.1-x86_64.AppImage
```

On Arch Linux or compatible distributions, install missing dependencies first if needed:

```bash
chmod +x arch_lib_install.sh
./arch_lib_install.sh
```

## Linux arm64

```bash
cd Linux/arm64/DMTool-v2.1.8.1-arm64
chmod +x start.sh
./start.sh
```

See [Linux/arm64/README.en.md](./Linux/arm64/README.en.md) for more details.

## MacOS

1. Open `MacOS/x86_64/` or `MacOS/arm64/` according to your chip architecture
2. Unzip the matching `.app.zip`
3. Run DMTool

If macOS blocks the app, allow it in "System Settings -> Privacy & Security".

## Maintenance Rules

- This directory only maintains the DMTool V2 host software for USB2CANFD / USB2CANFD-Dual.
- USB2CAN V1 host software and USB2CAN-specific materials are maintained in the USB2CAN module directory.
- When a version is updated, update `README.md`, `README.en.md`, and `CHANGELOG.md` together.
