# RXTX - Java 跨平台串口通信库

## 项目简介

RXTX 是一个为 Java 提供跨平台串行端口（Serial Port）和并行端口（Parallel Port）访问的开源库。

> 💡 **什么是串口？** 串口是计算机上一种传统的通信接口（如 COM1、COM2），常用于连接单片机、仪器仪表、工业设备等。RXTX 让 Java 程序能够与这些设备通信。

### 主要特性

- **跨平台支持**：支持 Linux、Windows、Mac OS、Solaris、FreeBSD、HP-UX 等多种操作系统
- **完整 CommAPI 实现**：遵循 Sun 的 [Java Communications API](https://docs.oracle.com/cd/E17802_01/products/products/javacomm/reference/api/)（简称 CommAPI）规范，提供 `gnu.io` 包的实现
- **串口和并口支持**：同时支持 RS232 串口通信和并口打印
- **事件通知**：支持串口事件监听（数据到达、载波检测、线路状态变化等）
- **流控支持**：支持硬件流控（RTS/CTS）和软件流控（XON/XOFF）
- **LGPL 许可证**：基于 GNU LGPL v2.1 开源发布，允许在各种项目中免费使用

> 📝 **什么是 CommAPI？**  
> CommAPI 是 Sun 公司制定的 Java 串口通信标准接口，定义了 `CommPort`、`SerialPort` 等类。RXTX 实现了这个接口，使得原本为 Sun 的 Java Communications 编写的代码可以直接使用 RXTX。

### 项目结构

```
rxtx/
├── rxtx-api/              # Java API 接口定义
├── rxtxSerial/            # 串口通信实现
├── rxtxSerial-java/       # Java JNI 代码
├── rxtxSerial-native/     # 跨平台原生库（C/C++）
├── rxtxSerial-linux-*/   # Linux 各架构支持
├── rxtxSerial-windows-*/ # Windows 支持
├── rxtxSerial-osx-*/     # macOS 支持
├── debian/               # Debian 包配置
└── cross-toolchain-wrapper/ # 跨平台编译工具链
```

> 📝 **什么是 JNI？**  
> JNI（Java Native Interface）是 Java 调用本地（C/C++）代码的接口。RXTX 通过 JNI 调用操作系统底层的串口 API，实现 Java 程序与硬件的通信。

### 支持的平台

| 构建平台 | 目标平台 | Linux | Windows | Mac OS |
|---------|---------|-------|---------|--------|
| **Linux x86** | x86 | ✅ | ✅ | ❌ |
| **Linux x86_64** | x86_64 | ✅ | ✅ | ❌ |
| **Linux arm** | arm | ✅ | ❌ | ❌ |
| **Mac OS x86_64** | x86_64 | ❌ | ❌ | ✅ |

### 版本说明

RXTX 版本号格式为 `RXTX-MAJOR.MINOR-PATCH`：

- **MAJOR（主版本）**：重大 API 变更，不兼容旧版本
- **MINOR（次版本）**：奇数为开发版（如 1.5、2.1），偶数为稳定版（如 1.4、2.2）
- **PATCH（补丁）**：同系列的 Bug 修复和小的改进

### 许可证

RXTX 基于 **GNU LGPL v2.1 + 受控接口例外**（Controlled Interface Exception）许可证发布：

- ✅ 库本身可以自由再发布和修改
- ✅ 通过 CommAPI 接口链接的程序不受 LGPL 限制
- ✅ 使用 RXTX 的独立模块可以采用任何许可证

> 📝 **什么是 LGPL？**  
> LGPL（Lesser General Public License）是 GNU 提供的一种开源许可证，比 GPL 更宽松。使用 LGPL 库时，即使修改了库本身，只要保留开源义务即可，但**链接**（使用） LGPL 库的程序不需要开源。

> 📝 **什么是"受控接口例外"？**  
> RXTX 通过 Sun 的 CommAPI 接口与应用程序链接。LGPL 的"受控接口例外"允许你通过这种标准接口使用 RXTX，而不必担心许可证传染问题。

完整许可证内容请参阅 [LICENSE.md](LICENSE.md)。

### 相关资源

- **官方网站**：http://www.rxtx.org
- **源码仓库**：https://github.com/rxtx/rxtx
- **邮件列表**：Majordomo@hex.linuxgrrls.org（发送 "subscribe rxtx" 订阅）

### 致谢

RXTX 是一个由众多开发者共同维护的开源项目。感谢所有贡献者的付出！详见 [AUTHORS.md](AUTHORS.md)。

---

*本项目由 Trent Jarvi (taj@www.linux.org.uk) 发起并维护。*

---

## 📎 文档导航

| ← 上一篇 | 🏠 首页 |下一篇 → |
|---------|--------|---------|
| — | [返回文档首页](index.md) | [安装指南](INSTALL.md) |
