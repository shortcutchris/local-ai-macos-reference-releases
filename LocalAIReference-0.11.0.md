# Local AI Reference 0.11.0

This release turns Skill Studio evaluations into complete, repeatable local
agent workflows rather than one-turn tool-choice checks.

- Codex can train a use case by versioning `SKILL.md`, typed tool contracts,
  fixtures, exact assertions, and an end-to-end Golden Path—without changing
  model weights.
- The included Excel/Business Central example makes the local model inspect and
  read a workbook, read bounded Business Central fixtures, call a deterministic
  reconciliation tool, create a new XLSX result, and reopen it for verification.
- Opaque handles pass data between tools, so the model orchestrates the process
  while the host performs exact row matching and file generation.
- Each model turn is a native typed function call, and only the dedicated
  completion function may finish the workflow; free-form model output is not
  accepted as an action.
- Skill Studio shows the complete tool order, sandbox approval, pass/fail
  assertions, verified workbook, and a Finder action for the generated result.
- The new training playbook defines how Codex should build and improve future
  API, spreadsheet, document, and business-system skills.

End-to-end tests remain safely local: they use bounded fixtures, deny external
writes and network access, cannot read credentials or arbitrary paths, and may
write only a new approval-gated XLSX file inside a private test directory. Live
Excel or Business Central access still requires a separately reviewed connector
and the normal user approval flow.
