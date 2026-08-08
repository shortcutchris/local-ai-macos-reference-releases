# Local AI Reference 0.12.0

This update makes local skill development visible and auditable for business
users.

- A completed Skill Studio run can now be published from the bundled CLI or MCP
  bridge as a clearly marked **Skill training** chat.
- The record shows the actual questions, bounded local evaluation data,
  immutable revision, chosen local model, ordered tools, assertions, exact
  counts, verified Excel artifacts, and the exact tested `SKILL.md` snapshot.
- The bridge still cannot read existing chats or submit arbitrary chat text. It
  can publish only an app-generated record for a completed run, once per run.
- Seven new local SME examples join the existing Excel/Business Central
  reconciliation: supplier-price auditing, payment matching, quality-complaint
  triage, confidential management-report analysis, contract/playbook review,
  tender compliance, and business-plan challenge. Eight complete Golden Paths
  are ready for local Qwen evaluation.
- The four confidential-document examples use synthetic PDF/table fixtures with
  source citations and create verified local Excel review artifacts. They cover
  business data categories that current KfW, IHK, WKO, and
  Mittelstand-Digital guidance identifies as both practical and sensitive.
- A localized Demo Portfolio menu in Skill Studio lets you explicitly add any
  of the eight verified examples as a local inactive draft. This action does
  not load a model, run a tool, install a skill, or use the network.
- Exact matching, financial arithmetic, date checks, quality thresholds, clause
  comparison, tender status, assumption flags, and XLSX creation remain
  deterministic host operations. Golden Paths expose only the one reviewed
  function allowed at each checkpoint and permit completion only after output
  verification. Malformed calls receive bounded format-only corrections and,
  only after those fail, one local inference-client restart with the same
  narrow capability. The host never chooses a business tool for the model.
  Separate routing tests measure unguided selection. The model never calculates
  or invents business results itself.

All bundled example data stays synthetic and local. Live Business Central,
bank, supplier, document-extraction, or production data still requires
separately reviewed connectors, normal user approvals, and credentials outside
every skill bundle.
