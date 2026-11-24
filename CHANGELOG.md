# 更新日志

## [v0.4.6](https://github.com/jiangxinlei/DeskChatGPT/releases/tag/v0.4.6)

### 更新

- 「连接设置 → 终端与 Git → 执行模式」新增原生执行，供 SwiftPM、Xcode 等需要自行启用沙箱的工具使用。默认使用受保护执行，原生执行需要在 Mac 上确认身份，仅对当前连接和服务会话生效。
- 终端任务详情可显示活跃任务及当前可见子进程的内存占用。关闭任务所属上下文或撤销目录授权时，DeskChatGPT 会停止相关任务，并报告清理未确认的情况。

### 安装包

- 提供 macOS 26 及以上的 Apple Silicon 和 Intel DMG、SHA-256 校验文件、中英文 EULA 和第三方组件许可证。两份安装包均使用本地证书签名，未经 Apple 公证。

## [v0.4.5](https://github.com/jiangxinlei/DeskChatGPT/releases/tag/v0.4.5)

### 修复

- 修复 Tunnel 客户端意外退出后，先前发起的连接检查可能取消自动重连的问题。
- 连接检查会区分本机服务无响应和远端轮询停滞，避免仅因诊断数据暂时不可用就将连接标为中断。
- 自动重连前再次检查 Tunnel，避免重启已经自行恢复的连接。

### 安装包

- 提供 macOS 26 及以上的 Apple Silicon 和 Intel DMG，以及 SHA-256 校验文件。两个安装包均使用本地证书签名，未经 Apple 公证。
- Apple 芯片版通过本机桌面回归。Intel 版在 Rosetta 下完成同一组桌面操作约需 99 秒，超过测试默认的 60 秒时限，延长等待后全部断言通过。Intel 实机及 Mac 睡眠唤醒后连回原 Tunnel 仍待验证。

## [v0.4.4](https://github.com/jiangxinlei/DeskChatGPT/releases/tag/v0.4.4)

### 修复

- 修正 Tunnel 连接状态和诊断时间，准确显示最近一次成功连接的时间。
- 调整睡眠唤醒后的连接恢复判断，避免检查间隔过长时反复重置失败计数。
- 合并界面和后台的重复连接检查，避免重复计数和重复触发恢复。

### 安装包

- 提供 macOS 26 及以上的 Apple Silicon 和 Intel DMG，以及 SHA-256 校验文件。
- 两份镜像均使用本地证书签名，包含中英文 EULA 和第三方组件许可证，未经 Apple 公证。
- Apple 芯片版通过本机桌面回归，Intel 版通过 Rosetta 桌面回归。Intel 实机和 Mac 实际睡眠唤醒后的连接恢复仍待验证。

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
