# Local Review to Markdown

[![VS Marketplace](https://img.shields.io/badge/VS%20Marketplace-Install-0B5FFF?logo=visualstudiocode&logoColor=white)](https://marketplace.visualstudio.com/items?itemName=tmsdnl.local-review-md)
[![Open VSX](https://img.shields.io/badge/Open%20VSX-Install-FC6D26)](https://open-vsx.org/extension/tmsdnl/local-review-md)

Turn inline code review notes into a structured Markdown file — ready to drop into any AI tool as context.

Annotate files using VS Code's native comments UI, organize notes into named review groups with drag and drop, and click export. The saved Markdown captures file paths, code excerpts, and Git metadata. Because it lives in your workspace, it is automatically available the next time you open an AI conversation.

Review state is stored in VS Code workspace extension storage and never written into project files. Markdown exports are written to `.review/` only when export is run.

## Use

1. Open a file-backed workspace.
2. Use the editor gutter comment action, or select code and run `Local Review: Add Review Note`.
3. Write the review note in the native VS Code comments UI.
4. Open the `Local Review` Activity Bar view to open, resolve, reopen, dismiss, copy, delete, or move notes between local reviews.
5. Run `Local Review: Export Markdown` from the view title or command palette.

The exported Markdown includes open and stale notes, file locations, excerpts, and Git metadata when the workspace is trusted and Git is available.

## Privacy

Review state stays on the local machine in VS Code workspace extension storage. The extension has no telemetry and no network service integration.

In untrusted workspaces, Git metadata capture is disabled. Local review notes and Markdown export still work for file-backed workspaces.

## Limitations

- Virtual workspaces are not supported.
- Reviews are local to the VS Code workspace storage.
- Exported Markdown is written into `.review/` in the workspace folder.
- Resolved and dismissed notes are kept in local state but omitted from the default Markdown export.
