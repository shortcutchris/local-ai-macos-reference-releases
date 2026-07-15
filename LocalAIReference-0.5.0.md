# Local AI macOS Reference 0.5.0

The app now recommends a local model from the Mac's detected chip and unified memory without telemetry or automatic downloads. Qwen 3.5 9B is the balanced tools-and-skills default, Qwen 3.5 35B-A3B is the premium 64 GB tier, and Qwen 3 Coder 30B-A3B is clearly separated as a coding specialist.

PDF, TXT, Markdown, JSON, and CSV files can be picked or dropped into chat. The app extracts bounded text locally, loads only the document skill needed for that request, and grants one opaque attachment to one typed read-only tool. Unknown or repeated tool calls are rejected, document content is treated as untrusted data, cancellation never commits a partial answer, and the source path is never sent to the model.

A new Tools & Skills Settings tab makes every capability boundary visible. Web search appears as a disabled design example because transmitting a search query would contradict the current local-only content promise; it remains unregistered until a separate provider, disclosure, and per-request approval flow is implemented.
