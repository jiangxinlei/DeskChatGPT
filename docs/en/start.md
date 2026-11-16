# Getting started

Follow these steps for your first setup. Your conversations remain in ChatGPT; DeskChatGPT supplies locally authorized tools.

## 1. Install and open DeskChatGPT

Download the DMG for your Mac from the [v0.4.3 release](https://github.com/jiangxinlei/DeskChatGPT/releases/tag/v0.4.3). It requires macOS 26 or later. Drag DeskChatGPT.app into Applications and open it. The installers use a local signing certificate and lack Apple notarization, so macOS may show a security prompt. The release page includes checksums and test results.

## 2. Create a Tunnel and limited runtime key

1. In [OpenAI Platform → Tunnels](https://platform.openai.com/settings/organization/tunnels), create a Tunnel and associate it with the correct ChatGPT workspace.
2. Copy the identifier beginning with `tunnel_`.
3. In [OpenAI Platform → API keys](https://platform.openai.com/settings/organization/api-keys), create a restricted key with only **Tunnels → Read + Use**. Never paste it into chat.

## 3. Connect your Mac

Open Connection settings and enter the Tunnel ID. Paste the runtime key only into the native Mac prompt. If you choose to remember it, the app protects the saved encrypted value with macOS Keychain. Continue once the connection status says the computer is connected.

## 4. Install your custom MCP tool in ChatGPT

Open [ChatGPT Plugins](https://chatgpt.com/plugins) in the associated workspace. Add a custom MCP server called DeskChatGPT, select the Tunnel connection and the same Tunnel ID. Local folder and write access are still controlled by the Mac app. Choose the tool in Chat mode using `@`.

## 5. Grant a folder, starting read-only

In Workbench, choose Add folder and select a disposable test directory without sensitive data. Read-only is the safer default. Use per-change approval if you want to modify files; direct read/write does not require each change to be confirmed.

## 6. Read and edit a test file

Create `README.md` in your test folder and ask:

> Use DeskChatGPT to read README.md from my test folder and show me its contents.

For an edit, ask ChatGPT to prepare a change, review the path and diff in the local app, approve it, and then continue in the original conversation. Deleted files do not go to Trash.

## 7. Review activity and revoke access

Use Activity to inspect operations and outcomes. In Workbench, adjust or remove folder permissions. Connection, terminal, browser, and desktop capabilities are managed separately.

See [Permissions and security](safety.md) and [Data and privacy](privacy.md) for limitations.
