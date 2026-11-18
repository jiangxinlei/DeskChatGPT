# 更新日志

## [v0.4.4](https://github.com/jiangxinlei/DeskChatGPT/releases/tag/v0.4.4)

### 修复

- Tunnel 健康检查使用客户端上报的真实成功轮询时间，避免将重复读取旧指标的时间记为最近成功时间。
- 使用 macOS 唤醒事件触发恢复宽限期，避免后台检查间隔较长时反复清零失败计数。
- 合并同时发生的界面与后台健康检查，避免重复累计失败和重复触发恢复。

### 安装包

- 提供 macOS 26 及以上的 Apple Silicon 和 Intel DMG，以及 SHA-256 校验文件。
- 两个架构均使用同一本机代码签名证书，包含中英文 EULA 和第三方组件许可证，未经 Apple 公证。
- Apple 芯片版通过本机桌面回归，Intel 版通过 Rosetta 桌面回归。实际睡眠唤醒后的恢复、Intel 实机及完整 ChatGPT 端到端验收仍待完成。

### Fixes

- Use the Tunnel client's actual successful poll timestamp for health checks and diagnostics.
- Apply the recovery grace period on a macOS resume event, avoiding repeated resets during infrequent background checks.
- Share concurrent UI and background health probes to avoid counting the same probe failure more than once.

## [v0.4.3](https://github.com/jiangxinlei/DeskChatGPT/releases/tag/v0.4.3)

### 功能
- 在 ChatGPT 对话中使用经过授权的本机文件、终端与 Git、独立浏览器和 macOS 桌面工具。
- 目录支持只读、逐项确认和直接读写；记录任务状态、变更回执与适用的恢复操作。
- 支持为不同 Mac 配置独立 Tunnel，并在 ChatGPT 中选择目标电脑。
- 提供中英文界面、使用文档和通过 `ads.json` 配置的广告位。

### 改进
- 优化 Tunnel 连接监测、异常恢复和原生桌面授权体验。
- 发布 macOS Apple Silicon 与 Intel x64 安装包及 SHA-256 校验文件。
- 空广告位支持手形光标，点击打开 [Canofold](https://canofold.dev/)。

安装包完整性检查不代表全部实机、权限和 ChatGPT 端到端验收已通过；实际发布内容以对应 GitHub Release 为准。
