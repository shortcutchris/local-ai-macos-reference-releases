# Local AI Reference 0.13.0

This release adds the first business-facing use-case experience directly to
the main chat window.

- **Use cases** is now always available in the chat sidebar and explains all
  eight bundled confidential-data workflows.
- The library clearly separates an untested template, a run that still needs
  improvement, and a fully tested demo.
- **View demo** appears only after an installed local model passed the complete
  end-to-end workflow and created an independently verified result file.
- The demo opens like a real business chat: it shows the synthetic input, the
  reviewed user request, the local model's completed answer, understandable
  workflow steps, and verified XLSX output with a Finder action.
- The header shows the exact pinned skill and semantic version. Reopening the
  same run reveals the same immutable demo instead of silently changing it.
- Technical fixtures, tool IDs, assertions, and digests remain in a separate
  read-only audit report.
- **Use my data** is deliberately not enabled yet. It will become available
  only after the exact published skill and all required runtime tools are
  installed and ready with the ordinary file and one-shot approval controls.

Existing chats are migrated locally without losing messages, memory, or search
history. Browsing the library or viewing an existing demo starts no model,
download, connector, tool, or network request. No model weights are changed.
