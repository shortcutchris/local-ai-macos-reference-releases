# Local AI macOS Reference 0.6.4

This patch fixes stale answers for current events.

Every request now includes the Mac's current local date, date/time, and time zone
inside a compact code-owned runtime boundary. The model is instructed to compare
dated claims with that context and to prefer recent, dated tool evidence over
pretrained assumptions.

For a time-sensitive web search, the host may append only the local date and
`latest confirmed results` to the model's proposed `query`. The approval sheet
shows that exact transformed JSON before anything is sent. Large search results
also leave room for a second separately approved query when the first evidence is
generic or stale.

The Mac Studio regression uses Qwen 3.5 35B-A3B, the full Docker `default`
profile, Brave Search, and a 16,384-token context. It now requires the verified
2026 World Cup final answer, Spain versus Argentina, rather than merely accepting
non-empty output.
