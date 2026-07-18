# Local AI macOS Reference 0.8.0

This release introduces the first Pi-inspired local agent-runtime milestone
without adding Pi, Node.js, a daemon, an account, or cloud inference.

The embedded model now runs through a dedicated bounded `LocalAgentRuntime`.
Each request freezes its relevant local tools, sequences document and tool
work, keeps the existing one-shot MCP approval boundary, limits context use,
and commits only a complete visible answer. Tool definitions and executors use
one typed registry and one central validation/authorization path.

Qwen tool calls that arrive in the supported raw markup form are recovered and
still pass through the same selected catalog, JSON schema, transformed approval
payload, and executor policy. Empty or reasoning-only turns receive at most two
bounded no-thinking retries.

The Mac Studio release gate passed 116 tests with zero failures. Separate live
Qwen 35B gates passed at 16K and 262K context, and the final 16K Docker Brave
test completed two approved searches, returned a sourced Spain–Argentina
answer, and used zero swap.
