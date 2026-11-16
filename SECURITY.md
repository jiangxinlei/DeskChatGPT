# DeskChatGPT Security and Privacy

## Current distribution status

This directory contains a **review copy**, not a certified public production release. Platform acceptance and independent review must be performed on the exact asset before publishing. The maintainer has elected not to use Apple Developer ID signing or notarization.

## Permission boundaries

- File operations are checked against the selected workspace and the locally granted access. File modifications use saved plans, baseline checks and replay-resistant receipts.
- A separate native permission step is required for high-impact terminal, browser and desktop capabilities.
- The terminal executes under the OS account and is not a folder sandbox. Browser automation and desktop screenshots can return sensitive information to ChatGPT.
- The current macOS native guard limits symlink traversal and unsafe filesystem operations. **An external process can still race the final file baseline check and update within a shared directory.** This is an acknowledged limitation; untrusted shared folders must not be advertised as safe.

## Local data

State databases, grant records, encrypted runtime keys, screenshots, private profiles and recovery bytes must never be included in any download or repository commit.

## Reporting

Do not send runtime keys, private databases, file contents or unredacted screenshots in issue reports. The project is independently developed and not endorsed by OpenAI.
