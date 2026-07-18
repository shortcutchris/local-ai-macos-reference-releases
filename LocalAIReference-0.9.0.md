# Local AI macOS Reference 0.9.0

This release completes the Pi-inspired local agent architecture while keeping
inference embedded, local, and account-free. It does not add Pi, Node.js, a
daemon, cloud inference, or automatically downloaded resources.

Each Send now freezes one inspected resource snapshot. Ordered internal
lifecycle hooks, the typed registry, the central authorization policy, and a
structured context pipeline coordinate model turns and tools without allowing
Settings changes to alter work already in progress. Large search, JSON, table,
log, document, skill, and MCP results are reduced deterministically, retain
decisive dated evidence, and visibly state when the continuation is incomplete.
One model turn may request up to four tools; returned batches run sequentially,
and every call retains its own validation, authorization, approval, execution,
and result-budget boundary. If the bounded result budget or round limit removes
all tools, repeated Qwen tool-call markup is not executed again; a bounded
no-thinking recovery produces the visible answer from completed evidence or
states that the available evidence is insufficient.

Settings can install non-executable `.localai-extension` folders containing
bounded skills, prompt templates, and inactive MCP setup presets. The app shows
an explicit capability/file/digest review, checks every declared SHA-256 before
and during private transactional copying, validates the installed copy, and
leaves the bundle disabled. MCP presets never launch or approve anything; the
normal MCP configuration, discovery, and **Run once** boundaries still apply.

Resource diagnostics show origins, readiness, versions, short digest prefixes,
safe collisions, and integrity failures without displaying prompt, chat,
attachment, skill, credential, or tool-result content. Hostile MCP descriptors,
oversized results/errors, nested data, extension paths, symlinks, scripts,
unknown fields, digest changes, cancellation, approval, denial, and removal
have dedicated deterministic or UI coverage.

Five explicit Mac Studio live schemes reuse already installed models to verify
the Qwen agent/tool/document/skill matrix, Docker Brave Search, Auto-Compact,
262K context, and Whisper load/transcription/composer/cancellation/unload. No
live scheme downloads a model implicitly. The notarized release build now
requires passing deterministic/UI and live evidence bound to the SHA-256
identity of the exact source tree, so stale green results cannot authorize a
different build.

Cancellation now terminates the underlying llama.cpp response producer before
the runtime can be reused. Auto-Compact cancellation therefore cannot leave a
background decode racing the next chat or Metal teardown. The Whisper live
fixture also uses an explicit installed macOS voice and temporary 16-kHz WAVE
audio for deterministic local lifecycle coverage.
