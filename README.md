<div align="center">

<img src="assets/logo.svg" alt="DeskChatGPT" width="88">

# DeskChatGPT

让 ChatGPT 连接你的 Mac，完成你授权的本机任务。

[功能特点](#功能特点) · [下载](#下载) · [使用](#使用) · [交流与支持](#交流与支持)

</div>

## 功能特点

- **文件与项目**：浏览目录、搜索文件、读取内容；创建、修改、移动、删除文件，支持批量改动、差异确认及适用的恢复操作。
- **终端与 Git**：执行命令、构建和测试，查看任务输出与运行状态，按需停止任务。
- **独立浏览器**：打开和阅读网页，点击、填写表单及截图。
- **桌面控制**：查看和打开应用，截图、操作鼠标与键盘，需获得 macOS 系统授权。
- **灵活的权限管理**：目录支持只读、逐项确认和直接读写；终端、浏览器与桌面能力分别授权。
- **多台 Mac**：为不同电脑配置独立连接，在 ChatGPT 中选择要使用的 Mac；文件和授权不会自动同步。
- **操作记录**：查看任务状态、文件变更和执行回执，方便核对结果和排查问题。

## 下载

各平台安装包统一从 [GitHub Releases](https://github.com/jiangxinlei/DeskChatGPT/releases) 获取。

| 系统    | 架构                   | 安装包 | 当前进度                                   |
| ------- | ---------------------- | ------ | ------------------------------------------ |
| macOS   | Apple Silicon（arm64） | DMG    | 安装包已构建并通过完整性校验，实机验收待完成 |
| macOS   | Intel（x64）           | DMG    | 安装包已构建并通过完整性校验，Intel 实机验收待完成 |
| Windows | x64                    | EXE    | 原生适配与安装包开发中，暂不提供下载       |

## 使用

1. 在 OpenAI Platform 创建私有 Tunnel，并在 DeskChatGPT 中连接当前 Mac。
2. 在 ChatGPT 工作区添加对应的自定义 MCP 工具。
3. 在 DeskChatGPT「工作台」授权需要访问的目录，建议先选择**只读**。
4. 在 ChatGPT 中选择 DeskChatGPT，开始读取文件或处理项目；需要修改时可选择逐项确认。

详细步骤见 [快速上手](docs/zh/start.md)。

## 使用文档

[产品介绍](docs/zh/overview.md) · [快速上手](docs/zh/start.md) · [授权与安全](docs/zh/safety.md) · [数据与隐私](docs/zh/privacy.md) · [常见问题](docs/zh/faq.md)

> 终端与 Git 使用当前系统用户权限，工具结果可能返回 ChatGPT。详细权限与限制见 [安全说明](SECURITY.md)。

## 交流与支持

问题与建议：[GitHub Issues](https://github.com/jiangxinlei/DeskChatGPT/issues)。欢迎为项目点一个 Star。

### 加群交流

<img src="assets/wechat.png" alt="加群交流" width="260">

### 请作者喝杯咖啡

如果 DeskChatGPT 帮到了你，欢迎请作者喝杯咖啡。

<img src="assets/sponsor.jpg" alt="请作者喝杯咖啡" width="240">
