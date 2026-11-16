# Permissions and security

## Choose folder permissions

| Mode                     | Meaning                                                                                            |
| ------------------------ | -------------------------------------------------------------------------------------------------- |
| Read only                | List, search, and read only within the authorized folder and its children                          |
| Read/write with approval | Prepare a change plan; inspect and approve each write on your Mac                                  |
| Direct read/write        | Create, update, move, or delete within the authorized folder without an individual approval dialog |

**Grant only the directories required for the task.** Changing or revoking a grant invalidates unexecuted related plans. The model cannot extend its own privileges.

## File changes and recovery

- Review the folder, target file, before/after content, and full hashes before approval. Deleted files do not go to Trash.
- Ordinary file creation and full replacement content is limited to **64 KiB**; authorized reads, exact patches, and deletion of regular UTF-8 files support up to **8 MiB**.
- A batch can contain at most 20 changes and runs sequentially. A failure does not automatically undo completed changes.
- If a file changed again after an operation, recovery may conflict. Never replay a write with an unknown outcome without inspecting the disk state.
- Reviewing an unknown outcome records evidence and a decision; **it does not execute the write again**.

## Separate capabilities

**Terminal and Git** run with your OS account and are **not sandboxed to a selected folder**. They can access other files and networks; grant and stop them independently.

**Isolated browser** actions can read webpages, click links, and submit forms. Review sensitive sign-ins, purchases, and submissions yourself.

**Desktop control** needs the appropriate macOS Screen & System Audio Recording and Accessibility permissions. Close sensitive windows before taking screenshots.

## Known security limitations

The native file guard rejects several unsafe links and path escapes, but **a non-cooperating external writer** can still race a final baseline check and file update within a shared folder. Do not advertise untrusted shared folders as securely isolated. Keep backups and review the repository's [Security policy](https://github.com/jiangxinlei/DeskChatGPT/blob/main/SECURITY.md).
