# 快速上手

首次使用请按顺序完成。DeskChatGPT 负责本机工具，聊天仍在 ChatGPT 中进行。

## 1. 安装并启动

从 [v0.4.3 发布页](https://github.com/jiangxinlei/DeskChatGPT/releases/tag/v0.4.3) 下载与你的 Mac 芯片匹配的 DMG。系统需要 macOS 26 或更新版本。将 DeskChatGPT.app 拖到「应用程序」并打开。安装包使用本地证书签名，未经 Apple 公证，首次打开时可能出现 macOS 安全提示。发布页列出了校验值和已完成的测试。

## 2. 创建 Tunnel 与受限运行密钥

1. 打开 [OpenAI Platform → Tunnels](https://platform.openai.com/settings/organization/tunnels)，选择所属组织并创建 Tunnel，关联 ChatGPT 工作区。
2. 复制 `tunnel_` 开头的 Tunnel ID。
3. 在 [OpenAI Platform → API keys](https://platform.openai.com/settings/organization/api-keys) 创建只具备 **Tunnels → Read + Use** 的运行密钥。不要发到聊天里。

## 3. 在 App 中连接电脑

进入「连接设置」，填写 Tunnel ID 并选择连接；运行密钥只在 Mac 原生确认窗口输入。勾选「记住密钥」后，App 将其加密保存并由 macOS 钥匙串保护。确认显示「电脑已连接」。

## 4. 在 ChatGPT 安装自定义 MCP 工具

打开 [ChatGPT 插件设置](https://chatgpt.com/plugins)，在关联工作区添加自定义 MCP 服务器。名称填写 DeskChatGPT，连接方式选择 Tunnel，使用同一 Tunnel ID；本机授权仍由 DeskChatGPT 管理。之后在 Chat 模式通过 `@` 选择该工具。

## 5. 添加目录，优先选择只读

在「工作台」点击「添加目录」，在 Mac 窗口选择一个**没有敏感内容的测试文件夹**。默认建议「只读」。如需修改文件，可选择「读写 · 逐项确认」；「直接读写」无需逐项审批，风险更高。

## 6. 首次读取与修改

可在测试目录创建一个 `README.md`，然后在 ChatGPT 中发送：

> 使用 DeskChatGPT 读取测试文件夹里的 README.md，并把内容显示给我。

如需修改，先使用「逐项确认」模式，请 ChatGPT 生成改动计划。在 App 中核对路径、文件差异并批准，再让原对话继续执行。实际删除不会进入废纸篓。

## 7. 查看结果与撤销授权

在「操作记录」检查改动和回执；在工作台找到目录，使用「管理权限」调整读写权限或「停止访问此目录」。如需停止 Tunnel，在「连接设置」操作。终端、浏览器、桌面权限是独立开关，不能用目录授权代替。

详细规则见 [授权与安全](safety.md) 和 [数据与隐私](privacy.md)。
