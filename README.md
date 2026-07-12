# Mi8E-Unlocker 全自动版

<p align="center">
  <b>面向 Snapdragon 8 Elite 小米设备的 Windows 一键 BL 解锁辅助工具</b>
</p>

<p align="center">
  <a href="https://t.me/Kernix_dev">
    <img src="https://img.shields.io/badge/Telegram-Kernix_dev-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>
  <img src="https://img.shields.io/badge/Platform-Windows-blue?style=for-the-badge&logo=windows&logoColor=white" alt="Windows">
  <img src="https://img.shields.io/badge/SoC-Snapdragon%208%20Elite-red?style=for-the-badge" alt="Snapdragon 8 Elite">
  <img src="https://img.shields.io/badge/System-HyperOS%202%2B-orange?style=for-the-badge" alt="HyperOS 2+">
  <img src="https://img.shields.io/badge/Patch-%E2%89%A4%202026--02--01-yellow?style=for-the-badge" alt="Patch">
</p>

---

## 📌 项目简介

**Mi8E-Unlocker** 是一款专为搭载 **骁龙 8 至尊版 / Snapdragon 8 Elite** 平台的小米设备打造的 **Windows 全自动 BL 解锁辅助工具**。

本项目通过 `toUnlock.bat` 脚本提供自动化引导流程，集成 ADB / Fastboot 环境、机型适配资源、状态检测工具与调试入口，用于在符合条件的 HyperOS 系统环境下完成 BL 解锁辅助操作。

当前工具适用于 **HyperOS 2.0 及以上**，且安全补丁级别不高于 **2026-02-01** 的系统环境。

> 如需帮助或交流，欢迎加入频道：  
> **https://t.me/Kernix_dev**

---

## ✨ 核心特性

- **Windows 一键运行**  
  直接运行 `toUnlock.bat` 即可进入自动化流程。

- **面向 Snapdragon 8 Elite 平台**  
  针对小米新一代旗舰平台设备进行适配。

- **多机型精准匹配**  
  脚本会根据选择的机型调用对应目录资源。

- **内置 ADB / Fastboot**  
  无需单独配置 Android Platform Tools。

- **BL 状态检测**  
  提供 `check-unlock.bat`，用于检测 BL 锁与工程 ABL 状态。

- **调试工具集成**  
  提供 `adb-tool.bat`，方便执行 ADB / Fastboot 调试命令。

- **中文交互提示**  
  内置完整中文提示，包含设备连接、环境检测、机型确认与风险提醒。

---

## 📱 已支持机型

当前已适配以下 **6 款 Snapdragon 8 Elite 平台设备**：

### Xiaomi 系列

- **Xiaomi 15**
- **Xiaomi 15 Pro**
- **Xiaomi 15 Ultra**

### Redmi 系列

- **Redmi K80 Pro**
- **Redmi K90**

### Tablet 平板系列

- **Xiaomi Pad 8 Pro**

---

## 🧩 系统要求

使用前请确认设备符合以下条件。

| 项目 | 要求 |
|---|---|
| 电脑系统 | Windows 10 / Windows 11 |
| 手机系统 | HyperOS 2.0 及以上 |
| 安全补丁 | 2026-02-01 及以前 |
| 设备平台 | Snapdragon 8 Elite |
| 连接方式 | USB 数据线 |
| 调试状态 | USB 调试已开启 |

---

## ⚠️ 兼容性说明

### 系统版本

支持：

```text
HyperOS 2.0 及以上
```

不支持：

```text
HyperOS 1.0 及更早版本
```

由于 HyperOS 1.0 及更早版本缺少相关底层服务组件，因此本工具流程无法在旧版本系统上正常生效。

### 安全补丁级别

支持范围：

```text
2026-02-01 及以前安全补丁
```

不支持范围：

```text
高于 2026-02-01 的安全补丁
```

自 2026-02-01 之后的补丁版本中，相关 SELinux 提权路径已被官方修复，因此该工具在更高补丁版本上可能无法完成对应流程。

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
    │   ├── Redmik90/
    │   ├── Xiaomi15/
    │   ├── Xiaomi15pro/
    │   ├── Xiaomi15ultra/
    │   └── Xiaomipad8pro/
    └── unlockGPT/
        ├── Xiaomipad8pro/
        └── else/
```

---

## 📁 主要文件说明

| 文件 / 目录 | 说明 |
|---|---|
| `toUnlock.bat` | 一键启动入口 |
| `8e-unlock.bat` | 主解锁流程脚本 |
| `check-unlock.bat` | BL 锁 / 工程 ABL 状态检测脚本 |
| `adb-tool.bat` | ADB / Fastboot 调试工具 |
| `8750-Ennea.img` | 解锁流程相关镜像 |
| `adb.exe` | ADB 工具 |
| `fastboot.exe` | Fastboot 工具 |
| `AdbWinApi.dll` | Windows ADB 运行库 |
| `AdbWinUsbApi.dll` | Windows ADB USB 运行库 |
| `unlockFolder/factoryImages/` | 各机型 factory images / ABL / GPT 资源 |
| `unlockFolder/unlockGPT/` | 解锁 GPT 相关资源 |

---

## 🚀 使用方法

### 1. 下载工具包

前往 **Releases** 页面下载最新版本：

```text
Mi8e-unlock-windows-auto-release.zip
```

### 2. 解压文件

请完整解压到本地目录。

推荐使用英文路径，例如：

```text
C:\Mi8E-Unlocker\
```

请勿直接在压缩包内运行脚本。

### 3. 开启 USB 调试

手机端开启：

```text
设置 → 关于手机 → 连续点击版本号开启开发者选项
设置 → 更多设置 → 开发者选项 → USB 调试
```

连接电脑后，请在手机弹窗中允许 USB 调试授权。

### 4. 启动解锁流程

双击运行：

```text
toUnlock.bat
```

根据脚本提示选择机型并继续操作。

### 5. 检查解锁状态

解锁流程完成后，可运行：

```text
check-unlock.bat
```

该脚本会检测：

- BL 锁状态
- 工程 ABL 状态
- 当前设备连接状态
- 可能的异常情况

### 6. Debug / 调试

如需手动执行 ADB / Fastboot 命令，可运行：

```text
adb-tool.bat
```

---

## ⚠️ 注意事项

- 解锁 BL 会清除所有用户数据，请务必提前备份。
- 请使用原装或质量稳定的数据线。
- 建议连接电脑后置 USB 2.0 接口。
- 请完整解压工具包后再运行脚本。
- 请勿删除、移动或重命名工具包内的文件。
- 不建议在虚拟机、远程桌面或不稳定 USB 环境中运行。
- 若设备无法识别，请检查 USB 调试授权、驱动和数据线。
- 不保证所有系统版本、区域版本或设备状态均可正常使用。

---

## ❓ 常见问题

### Q：运行脚本后提示未识别设备怎么办？

请检查：

- 是否已开启 USB 调试
- 手机是否弹出 USB 调试授权窗口
- 是否点击允许调试
- 数据线是否支持数据传输
- Windows 驱动是否正常
- 是否被其他手机助手占用 ADB
- 是否完整解压工具包

### Q：HyperOS 1.0 可以使用吗？

不支持。

本工具要求 HyperOS 2.0 及以上系统环境。

### Q：2026-02-01 之后的补丁可以使用吗？

不建议。

2026-02-01 之后的补丁版本中，相关路径已被官方修复，工具可能无法完成预期流程。

### Q：解锁会清除数据吗？

会。

BL 解锁会清除用户数据，请务必提前备份。

### Q：为什么建议使用英文路径？

部分批处理脚本和 ADB / Fastboot 工具在中文路径或特殊字符路径下可能出现异常。

推荐路径：

```text
C:\Mi8E-Unlocker\
```

---

## 💬 反馈与交流

如果你在支持机型上遇到以下问题：

- 设备未识别
- 脚本报错
- 状态检测异常
- 机型匹配错误
- ADB / Fastboot 通讯异常
- 流程中断或失败

请提交 **Issue**，并尽量附上：

- 设备型号
- 系统版本
- 安全补丁日期
- 脚本截图
- 报错内容
- 执行到哪一步失败
- 当前设备模式：系统 / Fastboot

也可以前往频道交流：

> **https://t.me/Kernix_dev**

---

## 👥 贡献者名单

感谢来自 [@Littlenine](https://github.com/LittlenineEnnea) 的核心技术支持。

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/LittlenineEnnea">
        <img src="https://github.com/LittlenineEnnea.png" width="100px;" alt="LittlenineEnnea"/><br />
        <sub><b>Littlenine</b></sub>
      </a><br />
      <sub>💡 核心技术 / 💻 解锁 boot.img</sub>
    </td>
  </tr>
</table>

---

## ⚖️ 免责声明

本项目仅供技术交流、自有设备维护与授权测试使用。

使用本工具可能导致：

- 用户数据清除
- 设备异常
- 系统无法启动
- 保修状态变化
- 需要重新刷机恢复
- 其他不可预期问题

使用者应自行确认设备归属与使用授权，并自行承担全部风险。

开发者不对因使用本项目造成的设备故障、数据丢失、保修失效或其他直接 / 间接损失承担责任。

请勿将本项目用于未授权设备、非法用途或任何侵犯他人权益的行为。