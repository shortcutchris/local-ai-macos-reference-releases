# Local AI macOS Reference 0.7.1

This patch makes MCP web-search routing and Qwen recovery more reliable.

Natural German and English requests such as “checken”, “prüfen”, “nachsehen”,
“verify”, and current-information questions can now select a configured general
web-search tool without requiring the internal tool or provider name. Passing
the tool to the local model starts no network request; Docker MCP still pauses
for the existing **Run once** approval with the exact query.

If Qwen occasionally ends a turn with internal reasoning but no native tool
request or visible answer, the app now discards that provisional turn and
retries it once with thinking disabled. Completed tools are retained as context
and never executed again by the retry. If the second attempt is also empty, the
error offers concrete retry, New Chat, and model-selection actions.

The Mac Studio regression reproduces the reported World Cup conversation,
including the earlier incorrect “no tools” response, then verifies approved
Brave Search and the final Argentina–Spain answer at a 16K context.
