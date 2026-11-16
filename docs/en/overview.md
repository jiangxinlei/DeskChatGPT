# Product overview

**DeskChatGPT connects ChatGPT to capabilities you explicitly authorize on your Mac.** It is an independently developed desktop companion, not a chat application or an AI model. You stay in ChatGPT; DeskChatGPT receives local MCP tool calls, checks authorization, performs permitted actions, and returns the results.

It provides no ChatGPT account, model, or subscription and is not an official OpenAI product. **Availability in ChatGPT, Dot, or Codex depends on the specific entry point, connected tools, and actual grants; a locally connected status does not prove all tools work in every mode.**

## Five core capabilities

| Capability               | What you can do                                                                                                               | Required permission                                                                     |
| ------------------------ | ----------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| Local files and projects | List folders, search names/content, read, create, update, exact patch, move, delete, batch operations, and supported recovery | Explicitly granted folders; read-only, per-change approval, or direct-write policy      |
| Terminal and Git         | Run commands, builds and tests; inspect output, view/stop tasks, and execute Git operations                                   | Separately enabled; runs under your OS account and **is not confined to folder grants** |
| Isolated browser         | Open and read pages, click, fill forms, and capture page screenshots                                                          | Separately enabled; independent of daily browser profiles                               |
| macOS desktop            | List/open apps, capture the screen, and operate permitted windows                                                             | Separately enabled; additional macOS Accessibility and Screen Recording permissions     |
| Activity and recovery    | Review task state, grants, file-change receipts, and supported recovery                                                       | Stored locally; not a replacement for cloud conversation history                        |

## Typical workflows

- **Understand a project:** Grant a read-only source folder, then search and explain the codebase.
- **Make a reviewed change:** Use per-change file approval, inspect each diff, and independently enable Terminal/Git to build or run tests when necessary.
- **Process many files:** Work within an authorized directory. A partially successful batch is not automatically rolled back.
- **Use a browser or desktop:** Enable those capabilities separately. Webpage and screen content may be returned to ChatGPT, so avoid sensitive data.
- **Choose a computer:** Configure a distinct Tunnel and custom MCP tool for each Mac, and select the intended target in ChatGPT.

## How a local request works

```text
ChatGPT conversation → custom MCP tool → private Tunnel for this Mac
                     → DeskChatGPT local service → permissions and approval
                     → file / terminal / browser / desktop action
                     → results and receipts returned to ChatGPT
```

1. Create a private Tunnel on OpenAI Platform and configure its custom MCP tool in an eligible ChatGPT workspace.
2. Connect the Mac in Connection settings and grant the required folders in Workbench.
3. Enable Terminal, browser, or desktop separately if needed. Review local approval prompts yourself.
4. Initiate the task in ChatGPT; inspect operation receipts and supported recovery in Activity.
5. On a timeout or disconnect, inspect existing tasks and actual results first. **Unknown outcome does not mean no action occurred; never blindly replay a write.**

## Select between multiple Macs

Use separate installations, private Tunnels, runtime keys, and local grants for your home and office Macs. Named tools such as `@DeskChatGPT-Home` and `@DeskChatGPT-Office` let you select the intended online device in an eligible workspace.

Keys, folders, and grants are **not synchronized**; this selects a tool target, not shared storage or a built-in remote-desktop switch.

## The four app pages

- **Workbench:** Authorized folders, access policies, and file changes.
- **Connection:** Tunnel status and independent Terminal/Git, browser, and desktop capabilities.
- **Activity:** Task state, change receipts, unknown-result review, and local records.
- **Guide:** Overview, getting started, security, privacy, and FAQ.

## Permissions, privacy, and limitations

Folder modes are read-only, per-change approval, and direct read/write. The model cannot approve its own grants. Deleted files do not go to Trash. Terminal commands run under your OS user and are **not limited to authorized folders**.

Tool results, including files, webpage contents, command output, and screenshots, may be sent to the initiating ChatGPT conversation. This is not an entirely offline product. The macOS file guard is experimental and has not completed independent security assessment.

Continue with [Getting started](start.md), [Permissions and security](safety.md), [Data and privacy](privacy.md), and [FAQ](faq.md).
