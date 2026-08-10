# Local AI Reference 0.12.2

This patch makes local Skill training reproducible and easier to audit.

- A published **Skill training** chat is now a read-only record. It cannot
  receive ordinary messages, attachments, drops, or manual chat compaction.
- **Replay run** repeats the exact immutable skill revision, test suite, private
  fixtures, original installed model, and context. The result is stored as a
  separate comparison chat; the source record never changes. A running replay
  can be cancelled.
- **Compare model** runs those identical cases with another already downloaded
  model and reports improved, regressed, and unchanged checks.
- **Open in Skill Studio** jumps directly to the corresponding draft for review
  without interpreting or copying the chat transcript.
- The opt-in Developer Bridge supports the same operation through
  `training replay <run-id> [installed-model-id]` and the MCP tool
  `replay_training_run`.
- A repository-local agent skill now gives Codex a strict repeatable process for
  building new business use cases from deterministic instructions, typed
  tools, synthetic fixtures, assertions, Golden Paths, and verified artifacts.
- Qwen workflow runs are more resilient when the model emits its known
  XML-style function-call form; the same one-tool and schema checks still apply.
- In-app Help and the bundled static SME overview explain how replay and fair
  installed-model comparison work.

Replay remains fully local. It starts no implicit download, reads no ordinary
chat, exposes no credential, and never contacts a production connector.
