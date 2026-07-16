# Local AI macOS Reference 0.6.2

This patch fixes Docker MCP discovery in the normally installed, notarized app.

macOS launches graphical apps with a restricted executable search path. Docker MCP Gateway starts profile containers through a nested `docker` command and accesses Docker Desktop's credential helper, so version 0.6.1 could mark the gateway as enabled while caching zero tools.

Version 0.6.2 supplies a deterministic search path containing only Docker Desktop's resources and macOS system directories. Brave Search, Context7, Firecrawl, Playwright, and other configured profile servers can therefore be discovered from the installed app.

An empty discovery is now an error rather than a successful enablement. Existing empty configurations are shown as **Needs refresh** and remain unavailable to chat until Refresh discovers at least one usable tool.
