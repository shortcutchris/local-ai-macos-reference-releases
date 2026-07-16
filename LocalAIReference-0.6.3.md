# Local AI macOS Reference 0.6.3

This patch fixes local-model context overflows when a Docker MCP profile contains many tools.

Previously, every cached MCP JSON schema was sent to the model at once. The current `default` profile can expose roughly 48 usable tools, which made the first Qwen 35B request exceed its 16,384-token context before Brave Search could run.

Version 0.6.3 ranks tools against the current user message and sends only a bounded relevant subset. A request that explicitly names Brave Search therefore receives the general Brave web-search tool without carrying unrelated Playwright, Firecrawl, or Context7 schemas.

Tool, document, and skill results also share a cumulative context-aware budget. Oversized results are visibly marked as truncated inside the model context, while the complete host-side call still follows the normal approval and execution limits.
