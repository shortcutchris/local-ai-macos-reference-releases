# Local AI macOS Reference 0.6.1

This patch adds a safe, guided Docker MCP Gateway workflow.

The **Tools & Skills** settings tab now detects Docker Desktop and can add one named Docker MCP profile as a reviewed stdio gateway. Adding the preset does not start Docker, inspect tools, pull images, or contact a provider. Enablement shows the exact command before Docker may verify images and briefly start profile containers.

Docker MCP receives a separate visible permission boundary: the host gateway can reach Docker only through local Unix sockets, while profile-managed containers may use the network and credentials configured in Docker Desktop. Every tool call still requires **Run once** with the server, tool, boundary, and exact JSON arguments.

The preset accepts only Docker Desktop's validly signed `docker` executable, verifies server-image signatures, disables Docker call logging, and filters Docker's dynamic management tools—including `mcp-add`, `mcp-remove`, `mcp-exec`, and `code-mode`—so the model cannot expand its own server set or bypass individual approval.

A built-in four-step guide recommends small profiles and explains Brave Search, Playwright, Firecrawl, and GitHub boundaries. Manual network-denied local stdio servers remain available unchanged.
