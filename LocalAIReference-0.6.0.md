# Local AI macOS Reference 0.6.0

This release adds the first complete local Tools, Skills, and MCP workflow.

Qwen can now use typed built-in tools for document reading, deterministic calculation, current date/time, and progressive skill loading. Tool and skill activity stays visible in the chat, while model reasoning remains separate from the Markdown answer and collapses automatically.

The **Tools & Skills** settings tab can import local `SKILL.md` folders. Only bounded text from the skill and its allowed `references/` files is copied; scripts are never imported or executed.

Trusted local stdio MCP servers can be added without starting them. Enabling a server shows the exact command before inspecting its tools. Every actual MCP call pauses for a one-time approval showing the server, tool, permission boundary, and exact JSON arguments. The process receives no chat history implicitly, runs with network access denied, and stops after discovery or the approved call.

The agent loop validates schemas and arguments in the host, limits tool rounds, supports cancellation, and never turns provisional tool work into a partial assistant message. Remote MCP transports, web search, automatic approvals, background daemons, and credential injection remain disabled.

Whisper Large v3 Turbo also receives a local tokenizer-cache fix for systems where the default Documents folder is not accessible.
