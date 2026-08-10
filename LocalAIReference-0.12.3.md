# Local AI Reference 0.12.3

This patch makes Skill Studio results easier to understand and fixes the two
misleading reconciliation failures.

- Every completed evaluation now shows **Open as training chat** directly in
  Skill Studio. It works without enabling the Developer Bridge.
- The training chat starts with a readable summary: passed checks, verified
  result files, and a plain-language explanation of what still needs work.
- Raw fixture data, assertions, tool IDs, and the generated transcript are
  still available, but remain collapsed under the technical audit record.
- One-turn decision tests now treat reviewed fixture values as already
  available, state the isolated workflow phase clearly, and run without
  sampling randomness. Qwen can therefore select the next safe tool instead of
  asking for information that is only needed later in the workflow.
- MCP tool calling now also recovers Qwen's observed hybrid function-call
  format while retaining the same schema validation, user approval, and local
  execution boundaries.
- A verified complete XLSX workflow is shown as partial success when a separate
  routing check fails; it is no longer presented as if the result file itself
  had failed.
- Selected chat titles keep identical font metrics, preventing two-line titles
  from shifting the sidebar layout.

All training data, generated files, and model inference remain local. This
update adds no implicit download, network service, credential access, or new
connector authority.
