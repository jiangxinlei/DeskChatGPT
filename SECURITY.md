# DeskChatGPT Security and Privacy

## Current distribution status

Published macOS installers use a local signing certificate and are distributed without Apple notarization. See the corresponding release for the checks performed. The native file guard is experimental, and an independent production security review remains pending.

## Permission boundaries

- File operations are checked against the selected workspace and the locally granted access. File modifications use saved plans, baseline checks and replay-resistant receipts.
- A separate native permission step is required for high-impact terminal, browser and desktop capabilities.
- The terminal executes under the OS account and is not a folder sandbox. Browser automation and desktop screenshots can return sensitive information to ChatGPT.
- Protected execution is the default. In v0.4.6 or later, enabling native execution requires identity confirmation on the Mac. Native commands run with the current account's permissions and can access or modify DeskChatGPT's local state, credentials, and app files if that account can access them. ChatGPT cannot change this setting. Turning off terminal access or restarting the service restores protected execution. See [简体中文](docs/zh/safety.md#终端执行模式) and [English](docs/en/safety.md#terminal-execution-modes).
- The current macOS native guard limits symlink traversal and unsafe filesystem operations. **An external process can still race the final file baseline check and update within a shared directory.** This is an acknowledged limitation; untrusted shared folders must not be advertised as safe.

## Local data

State databases, grant records, encrypted runtime keys, screenshots, private profiles and recovery bytes must never be included in any download or repository commit.

## Reporting

Do not send runtime keys, private databases, file contents or unredacted screenshots in issue reports. The project is independently developed and not endorsed by OpenAI.
