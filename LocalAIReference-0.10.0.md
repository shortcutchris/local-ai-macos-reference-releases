# Local AI Reference 0.10.0

This release adds a complete local Skill Studio and Developer Bridge.

- Create and review versioned skill drafts with rollback.
- Declare typed tool and MCP contracts without embedding executable code or credentials.
- Run fixture checks or explicit decision tests with an already installed local model.
- Export a verified `.localai-extension`, then use the existing review before installation.
- Connect Codex or another local developer through the optional bundled CLI/MCP adapter while the app is running.
- Start with the included Excel reconciliation and read-only Microsoft Business Central example.

The Developer Bridge is off by default. It does not open a network service, cannot download models, cannot install or activate a skill, and cannot bypass normal tool approvals.
