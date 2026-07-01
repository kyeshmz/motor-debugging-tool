# DMTool Linux arm64

[中文](./README.md) | [EN](./README.en.md)

This package is the Linux `arm64` build of DMTool.

## Package Layout

Current directory:

- `bin/serial-port-assistant`: main executable
- `lib/`: bundled Qt and runtime libraries
- `plugins/`: Qt platform and image plugins
- `start.sh`: recommended launcher script

## Quick Start

From the extracted package directory:

```bash
chmod +x start.sh
./start.sh
```

`start.sh` sets:

- `LD_LIBRARY_PATH=$DIR/lib`
- `QT_PLUGIN_PATH=$DIR/plugins`

and then launches:

```bash
$DIR/bin/serial-port-assistant
```

## Arch Linux Dependencies

This package bundles most Qt libraries, but system graphics and X11-related runtime libraries are still required.

Recommended Arch install command:

```bash
sudo apt update &&
sudo apt install -y \
    libgl1-mesa-glx \
    libglu1-mesa \
    libegl1 \
    libx11-6 \
    libxcb1 \
    libxext6 \
    libxfixes3 \
    libxrender1 \
    libxrandr2 \
    libxdamage1 \
    libxinerama1 \
    libxkbcommon0 \
    libopengl0 \
    libxcb-cursor0 \
    libxcb-icccm4 \
    libxcb-keysyms1 \
    libxcb-image0 \
    libxcb-render-util0
```

Notes:

- `libglvnd` covers the OpenGL / EGL runtime side used here.
- `xcb-util-wm` is the Arch package corresponding to the Ubuntu `libxcb-icccm4` family.
- `xcb-util-renderutil` is the Arch package corresponding to Ubuntu `libxcb-render-util0`.

## Troubleshooting

If startup fails, check these first:

1. `start.sh` has execute permission.
2. `QT_QPA_PLATFORM` is appropriate for the environment.
3. Required system OpenGL / X11 / XCB libraries are installed.
4. You are launching through `start.sh` rather than calling `bin/serial-port-assistant` directly.
