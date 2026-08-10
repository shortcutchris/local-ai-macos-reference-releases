# Local AI Reference 0.12.4

This patch turns the former training-chat replay into a clear, guided business
demo while preserving its exact reproducibility and local safety boundaries.

- Completed Skill Studio runs now open as visibly read-only **audit reports**.
- Every report begins with a **Guided demo** card that explains the reviewed
  sample inputs, local model and tool execution, and independent verification.
- **Start guided demo** reruns the exact immutable skill revision, test suite,
  private fixtures, original installed model, and context. It creates a new
  comparable report and never changes the source report.
- Progress and cancellation stay visible while the local demo runs; a missing
  original model never triggers an implicit download.
- **Compare model** and **Open in Skill Studio** remain available as separate
  actions, while raw tool IDs, fixtures, assertions, and digests stay collapsed.
- Skill Studio, the built-in Help guide, the standalone SME page, and the
  English/German interface now use the same guided-demo and audit-report terms.
- A new concept document defines the later **Try it yourself** working-chat
  boundary without granting fixture, connector, or approval authority early.

All sample data, generated files, model inference, and result verification stay
local. The update adds no implicit model download, cloud service, credential
access, production connector call, or model-weight fine-tuning.
