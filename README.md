# RXTX 中文文档

## 仓库说明

这是 RXTX 库的中文文档仓库。RXTX 是一个为 Java 提供跨平台串行端口（Serial Port）和并行端口（Parallel Port）访问的开源库。

## 如何访问文档

### 在线访问

文档已部署到 GitHub Pages，您可以通过以下链接访问：
- **在线文档**：[https://yeatsliao.github.io/rxtx-docs-cn/](https://yeatsliao.github.io/rxtx-docs-cn/)

### 本地访问

1. **克隆仓库**：
   ```bash
   git clone https://github.com/YeatsLiao/rxtx-docs-cn.git
   cd rxtx-docs-cn
   ```

2. **使用浏览器打开**：
   - 直接在浏览器中打开 `index.md` 文件
   - 或使用支持 Markdown 预览的编辑器查看

## 文档结构

```
rxtx-docs-cn/
├── index.md                # 文档首页
├── project-overview.md     # 项目简介（原 README.md）
├── INSTALL.md              # 安装指南
├── SerialPortInstructions.md  # 串口使用教程
├── PORTING.md              # 移植指南
├── ChangeLog.md            # 变更日志
├── AUTHORS.md              # 贡献者名单
├── license-summary.md      # 许可证摘要（原 LICENSE.md）
├── full-license.md         # 完整许可证（原 COPYING.md）
├── wiki/                   # 额外文档
│   ├── Home.md
│   └── Supported-Build-Hosts.md
└── _config.yml            # GitHub Pages 配置
```

## 文档导航

### 入门
- [项目简介](project-overview.md)
- [安装指南](INSTALL.md)
- [串口使用教程](SerialPortInstructions.md)

### 参考
- [移植指南](PORTING.md)
- [支持的构建主机](wiki/Supported-Build-Hosts.md)
- [变更日志](ChangeLog.md)

### 关于
- [贡献者名单](AUTHORS.md)
- [许可证摘要](license-summary.md)
- [完整许可证](full-license.md)

## 项目特点

- **跨平台支持**：支持 Linux、Windows、Mac OS、Solaris、FreeBSD、HP-UX 等多种操作系统
- **完整 CommAPI 实现**：遵循 Sun 的 [Java Communications API](https://docs.oracle.com/cd/E17802_01/products/products/javacomm/reference/api/)（简称 CommAPI）规范，提供 `gnu.io` 包的实现
- **串口和并口支持**：同时支持 RS232 串口通信和并口打印
- **事件通知**：支持串口事件监听（数据到达、载波检测、线路状态变化等）
- **流控支持**：支持硬件流控（RTS/CTS）和软件流控（XON/XOFF）
- **LGPL 许可证**：基于 GNU LGPL v2.1 开源发布，允许在各种项目中免费使用

## 官方资源

- **官方网站**：http://www.rxtx.org
- **源码仓库**：https://github.com/rxtx/rxtx
- **邮件列表**：Majordomo@hex.linuxgrrls.org（发送 "subscribe rxtx" 订阅）

## 翻译说明

- 基于 RXTX 2.2（development 分支）
- 许可证以英文原版为准
- 欢迎提交 Issue 改进翻译

---

*本项目由 [YeatsLiao](https://github.com/YeatsLiao) 维护。*
