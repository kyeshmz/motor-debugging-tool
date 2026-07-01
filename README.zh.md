# DMTool（USB2CANFD）

[中文](./README.md) | [EN](./README.en.md)

本目录仅保留 USB2CANFD / USB2CANFD-Dual 使用的 DMTool V2 上位机资料。USB2CAN 相关上位机、开源协议、结构件和使用资料已归档到 USB2CAN 模块目录，不再在本目录重复维护。

USB2CAN 资料入口：`模块/通信模块/USB2CAN`

## 目录内容

| 平台 | 文件 | 说明 |
| --- | --- | --- |
| Windows x86_64 | `Windows/x86_64/DMTool 2.1.8.1.exe` | Windows 可执行程序 |
| Linux x86_64 | `Linux/x86_64/DMTool-v2.1.8.1-x86_64.AppImage` | Linux x86_64 AppImage |
| Linux x86_64 | `Linux/x86_64/arch_lib_install.sh` | Arch Linux 依赖安装脚本 |
| Linux arm64 | `Linux/arm64/DMTool-v2.1.8.1-arm64/start.sh` | Linux arm64 运行入口 |
| MacOS x86_64 | `MacOS/x86_64/DMTool-v2.1.8.1-x86_64.app.zip` | macOS Intel 包 |
| MacOS arm64 | `MacOS/arm64/DMTool-v2.1.8.1-arm64.app.zip` | macOS Apple Silicon 包 |
| 使用说明 | `DMTool上位机软件说明书.pdf` | 上位机软件说明书 |

## Windows

1. 进入 `Windows/x86_64/`
2. 双击运行 `DMTool 2.1.8.1.exe`
3. 首次运行如被系统拦截，选择“更多信息”后继续运行

## Linux x86_64

```bash
cd Linux/x86_64
chmod +x DMTool-v2.1.8.1-x86_64.AppImage
./DMTool-v2.1.8.1-x86_64.AppImage
```

如在 Arch Linux 或兼容发行版上缺少运行库，可先执行：

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

更多说明见 [Linux/arm64/README.md](./Linux/arm64/README.md)。

## MacOS

1. 根据芯片架构选择 `MacOS/x86_64/` 或 `MacOS/arm64/`
2. 解压对应 `.app.zip`
3. 双击运行 DMTool

如系统提示无法打开，可在“系统设置 -> 隐私与安全性”中允许本应用运行。

## 维护规则

- 本目录只维护 USB2CANFD / USB2CANFD-Dual 使用的 DMTool V2 上位机。
- USB2CAN V1 上位机和 USB2CAN 专属资料统一维护在 USB2CAN 模块目录。
- 更新版本时需同步更新 `README.md`、`README.en.md` 和 `CHANGELOG.md`。
