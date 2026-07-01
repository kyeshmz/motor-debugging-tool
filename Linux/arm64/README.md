# DMTool Linux arm64

[中文](./README.md) | [EN](./README.en.md)

这是 DMTool 的 Linux `arm64` 构建版本。

## 目录结构

当前目录包含：

- `bin/serial-port-assistant`：主程序
- `lib/`：打包的 Qt 及运行时库
- `plugins/`：Qt 平台插件和图像插件
- `start.sh`：推荐启动脚本

## 快速开始

在解压后的目录中执行：

```bash
chmod +x start.sh
./start.sh
```

`start.sh` 会自动设置：

- `LD_LIBRARY_PATH=$DIR/lib`
- `QT_PLUGIN_PATH=$DIR/plugins`

然后启动：

```bash
$DIR/bin/serial-port-assistant
```

## Arch Linux 依赖

本软件已打包大部分 Qt 库，但仍依赖系统提供的图形与 X11 相关运行时库。

推荐执行以下命令安装依赖：

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

说明：

- `libglvnd` 提供本程序所需的 OpenGL / EGL 运行时支持。
- `xcb-util-wm` 对应 Ubuntu 系列中的 `libxcb-icccm4`。
- `xcb-util-renderutil` 对应 Ubuntu 中的 `libxcb-render-util0`。

## 故障排查

如果程序启动失败，请优先检查以下项目：

1. `start.sh` 是否具有可执行权限。
2. `QT_QPA_PLATFORM` 是否适合当前运行环境。
3. 是否已安装所需的 OpenGL、X11 和 XCB 运行时库。
4. 请通过 `start.sh` 启动程序，而不要直接运行 `bin/serial-port-assistant`。
