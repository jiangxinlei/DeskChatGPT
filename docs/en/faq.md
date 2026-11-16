# Frequently asked questions

## The Mac says Connected, but ChatGPT cannot call DeskChatGPT

Confirm the ChatGPT workspace, custom MCP tool, and Tunnel ID match. Refresh the tool in Plugin settings and start a new Chat conversation. When disconnected, copy local diagnostics without including a runtime key.

## I cannot read a file or write to a folder

Verify that the folder is granted to the current connection. Read-only access does not allow writes. Per-change approval requires you to approve a plan on the Mac. Expired plans must be recreated after rereading the file.

## Why does recovery report a conflict?

The file may have changed or moved since the original edit, or its previous path may be occupied. Preserve the current data, examine the diff, and avoid blind overwrites.

## Why is an old screenshot missing its thumbnail?

Older records may contain activity metadata but no saved screenshot. Newer captures may also be rotated because of screenshot or activity limits. The originating ChatGPT conversation may contain the original tool result.

## Can I switch between my home and office Macs?

Yes. Install DeskChatGPT independently on both Macs, configure **a different private Tunnel for each**, and add two named custom MCP tools to the **same eligible ChatGPT workspace**. For example, name them `DeskChatGPT-Home` and `DeskChatGPT-Office`.

Choose `@DeskChatGPT-Home` or `@DeskChatGPT-Office` in ChatGPT to route a request to that online Mac. Each device must approve its own folders and operations. Tunnel keys, file access, and granted permissions are **not shared or synchronized**. Verify the chosen target before running a task.
