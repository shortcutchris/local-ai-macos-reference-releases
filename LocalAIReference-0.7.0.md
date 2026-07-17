# Local AI macOS Reference 0.7.0

This release adds durable, private chat history and context-aware memory.

The main window now includes a native conversation sidebar. Chats can be
created, searched, reopened after relaunch, renamed, and deleted with
confirmation. Empty drafts are not stored. Completed visible messages remain on
this Mac in a private SQLite database; deleting a chat also removes its local
search index and memory checkpoint.

Long conversations no longer depend on sending the entire transcript to the
model. At 70% projected context use, the app visibly and cancellably compacts
older messages into a validated structured memory, keeps the newest exchange
exact, and continues the original request. Relevant older details can be
reintroduced exactly from a bounded, chat-isolated local full-text index. The
complete transcript stays visible, and the header menu can inspect memory,
display advisory context use, or start compaction manually.

Everything remains on-device. Auto-Compact uses only an already installed local
model and never starts a download. Conversation storage excludes model
reasoning, provisional answers, raw tool/MCP data, attachment contents and
paths, audio, and credentials.

Mac Studio verification covers 98 tests including the conversation-sidebar UI
flow, a real Qwen 3.5 35B-A3B 16K compaction/retrieval flow, and the existing
full 262K Qwen load/generation gate.
