# Mi8E-Unlocker

<p align="center">
  <b>Snapdragon 8 Elite 小米设备 Windows 全自动 BL 解锁辅助工具</b>
</p>

<p align="center">
  <a href="https://t.me/Kernix_dev">
    <img src="https://img.shields.io/badge/Telegram-Kernix_dev-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>
  <img src="https://img.shields.io/badge/Platform-Windows-blue?style=for-the-badge&logo=windows&logoColor=white" alt="Windows">
  <img src="https://img.shields.io/badge/SoC-Snapdragon%208%20Elite-red?style=for-the-badge" alt="Snapdragon 8 Elite">
  <img src="https://img.shields.io/badge/System-HyperOS%202%2B-orange?style=for-the-badge" alt="HyperOS 2+">
  <img src="https://img.shields.io/badge/Status-Active-success?style=for-the-badge" alt="Status">
</p>

---

## 📌 项目简介

**Mi8E-Unlocker** 是一款面向 **Snapdragon 8 Elite 平台小米设备** 的 Windows 全自动 BL 解锁辅助工具。

本项目集成了解锁脚本、机型适配资源、ADB/Fastboot 工具、状态检测脚本与调试入口，旨在简化高版本 HyperOS 环境下的 BL 解锁流程，减少手动操作步骤，提高执行效率与可重复性。

用户只需在 Windows 环境下完整解压工具包，连接设备并运行 `toUnlock.bat`，即可根据脚本提示完成自动化流程。

> 如需帮助或交流，欢迎加入频道：  
> **https://t.me/Kernix_dev**

---

## 🚀 项目亮点

- **Windows 全自动流程**  
  通过 `toUnlock.bat` 启动，一键进入自动化解锁流程。

- **面向 Snapdragon 8 Elite 平台**  
  针对新一代小米旗舰平台设备适配。

- **多机型资源集成**  
  内置 Xiaomi / Redmi / Pad 多款设备适配资源。

- **内置 ADB / Fastboot**  
  无需用户额外安装 Android Platform Tools，解压即可使用。

- **BL 状态检测**  
  提供 `check-unlock.bat`，用于检测 BL 锁状态与工程状态。

- **调试工具入口**  
  提供 `adb-tool.bat`，方便进行 ADB / Fastboot 调试。

- **机型文件自动调用**  
  脚本会根据选择的机型调用对应 factoryImages 与 unlockGPT 资源。

---

## 📱 支持机型

当前 Release 内置以下机型资源：

| 系列 | 机型 |
|---|---|
| Xiaomi | Xiaomi 15 |
| Xiaomi | Xiaomi 15 Pro |
| Xiaomi | Xiaomi 15 Ultra |
| Redmi | Redmi K80 Pro |
| Redmi | Redmi K90 |
| Xiaomi Pad | Xiaomi Pad 8 Pro |

---

## 🧩 系统要求

| 项目 | 要求 |
|---|---|
| 电脑系统 | Windows 10 / Windows 11 |
| 手机系统 | HyperOS 2.0 及以上 |
| 设备平台 | Snapdragon 8 Elite |
| 连接方式 | USB 数据线 |
| 调试状态 | USB 调试已开启 |

### 不支持

- HyperOS 1.0 及更早版本
- 非 Snapdragon 8 Elite 平台设备
- 未列入支持列表的设备
- 无法被 ADB / Fastboot 正常识别的设备

---

## 📦 Release 包结构

```text
Mi8e-unlock-windows-auto-release.zip
├── 8750-Ennea.img
├── 8e-unlock.bat
├── toUnlock.bat
├── check-unlock.bat
├── adb-tool.bat
├── adb.exe
├── fastboot.exe
├── AdbWinApi.dll
├── AdbWinUsbApi.dll
├── 赞助一下谢谢喵.png
└── unlockFolder/
    ├── factoryImages/
    │   ├── Redmik80pro/
    │   │   └── images/
    │   │       ├── abl.elf
    │   │       └── gpt_both4.bin
    │   ├── Redmik90/
    │   │   └── images/
    │   │       ├── abl.elf
    │   │       └── gpt_both4.bin
    │   ├── Xiaomi15/
    │   │   ├── flash_all.bat
    │   │   └── images/
    │   ├── Xiaomi15pro/
    │   │   ├── flash_all.bat
    │   │   └── images/
    │   ├── Xiaomi15ultra/
    │   │   └── images/
    │   │       ├── abl.elf
    │   │       └── gpt_both4.bin
    │   └── Xiaomipad8pro/
    │       └── images/
    │           ├── abl.elf
    │           └── gpt_both4.bin
    └── unlockGPT/
        ├── Xiaomipad8pro/
        │   └── unlockgpt_both4.bin
        └── else/
            └── unlockgpt_both4.bin
```

---

## 📁 主要文件说明

| 文件 / 目录 | 说明 |
|---|---|
| `toUnlock.bat` | 一键解锁入口 |
| `8e-unlock.bat` | 主解锁流程脚本 |
| `check-unlock.bat` | BL / 工程状态检测脚本 |
| `adb-tool.bat` | ADB / Fastboot 调试工具 |
| `8750-Ennea.img` | 解锁流程相关镜像 |
| `unlockFolder/factoryImages/` | 各机型 factory images / ABL / GPT 资源 |
| `unlockFolder/unlockGPT/` | unlock GPT 文件目录 |
| `adb.exe` / `fastboot.exe` | Android 调试与 Fastboot 工具 |
| `AdbWinApi.dll` / `AdbWinUsbApi.dll` | Windows ADB 运行库 |

---

## 🛠️ 使用方法

### 1. 下载工具包

前往 **Releases** 页面下载最新版本：

```text
Mi8e-unlock-windows-auto-release.zip
```

### 2. 解压文件

请完整解压到本地目录，建议使用英文路径，例如：

```text
C:\Mi8E-Unlocker\
```

不要直接在压缩包内运行脚本。

### 3. 开启 USB 调试

手机端开启：

```text
设置 → 关于手机 → 连续点击版本号开启开发者选项
设置 → 更多设置 → 开发者选项 → USB 调试
```

连接电脑后，请在手机弹窗中允许 USB 调试授权。

### 4. 运行解锁脚本

双击运行：

```text
toUnlock.bat
```

根据脚本提示选择机型，并完成后续流程。

### 5. 检查解锁状态

解锁完成后，可运行：

```text
check-unlock.bat
```

用于检测 BL 锁状态与工程状态。

### 6. ADB / Fastboot 调试

如需手动使用 ADB / Fastboot，可运行：

```text
adb-tool.bat
```

---

## ⚠️ 注意事项

- 解锁 BL 会清除用户数据，请务必提前备份。
- 请使用原装或质量稳定的数据线。
- 建议连接电脑后置 USB 2.0 接口。
- 请完整解压工具包后再运行脚本。
- 请勿删除、移动或重命名工具包内的文件。
- 建议使用 Windows 10 / 11 运行。
- 不建议在虚拟机、远程桌面或不稳定 USB 环境中操作。
- 不保证所有系统版本、区域版本或设备状态均可正常使用。

---

## ❓ 常见问题

### 设备无法识别怎么办？

请检查：

- 是否开启 USB 调试
- 是否点击允许 USB 调试授权
- 数据线是否支持数据传输
- Windows 驱动是否正常
- 是否被其他手机助手占用 ADB
- 是否完整解压工具包

### HyperOS 1.0 可以使用吗？

不支持。  
本工具面向 HyperOS 2.0 及以上系统环境。

### 解锁会清除数据吗？

会。  
BL 解锁流程会清除用户数据，请务必提前备份。

### 为什么要使用英文路径？

部分 Windows 批处理、ADB/Fastboot 工具在中文路径、特殊字符路径下可能出现执行异常。  
建议解压到类似以下路径：

```text
C:\Mi8E-Unlocker\
```

### 脚本运行失败怎么办？

请保留报错截图，并反馈以下信息：

- 设备型号
- 系统版本
- 当前模式：系统 / Fastboot
- 脚本报错截图
- 执行到哪一步失败

---

## 💬 反馈与交流

如果你遇到设备未识别、脚本报错、状态检测异常等问题，请提交 Issue，或前往频道交流：

> **https://t.me/Kernix_dev**

---

## 👥 贡献者

感谢来自 [@Littlenine](https://github.com/LittlenineEnnea) 的核心技术支持。

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/LittlenineEnnea">
        <img src="https://github.com/LittlenineEnnea.png" width="100px;" alt="LittlenineEnnea"/><br />
        <sub><b>Littlenine</b></sub>
      </a><br />
      <sub>核心技术支持 / 解锁相关研究</sub>
    </td>
  </tr>
</table>

---

## ⚖️ 免责声明

本项目仅供技术交流、自有设备维护与授权测试使用。

使用本工具可能导致数据清除、设备异常、系统损坏、保修状态变化或其他不可预期后果。  
请在使用前确认设备属于你本人或已获得明确授权，并自行承担全部风险。

开发者不对任何滥用行为、设备损坏、数据丢失、保修失效或法律后果承担责任。

请勿将本项目用于未授权设备、非法用途或任何侵犯他人权益的行为。