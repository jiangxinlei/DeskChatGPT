# Data and privacy

## Local storage

On macOS, local user data is generally stored at:

`~/Library/Application Support/DeskChatGPT/state/`

It includes:

- `state.db`: local connections, grants, activity, screenshots, change plans, and supported recovery records.
- Remembered runtime keys: encrypted on disk only if you choose to remember them, with macOS Keychain protection.
- Private profiles and configuration: must not be uploaded to public repositories or shared in support requests.
- Database migration backups and `state.desktop/`: may remain following upgrades or Electron app usage.

## Retention

- Up to approximately **10,000 activity records**, with up to **100 screenshots**, subject to rotation.
- Bounded terminal/Git task metadata; an output segment is limited to around **64 KiB**, and in-memory output may disappear after a service restart.
- File recovery and outstanding change plans have a different retention scope from activity history. Clearing ordinary logs is not the same as undoing file changes.

## Managing and removing data

Use **Activity → Manage local records** to clear screenshots and activity separately. Workbench's old-data cleanup examines expired task records before applying changes.

To forget a saved runtime key, use Connection settings and revoke the original key in OpenAI Platform if required. Content already sent to ChatGPT must be managed in ChatGPT separately; deleting local records cannot remove cloud conversations.
