# Local AI macOS Reference 0.6.5

This patch makes the embedded model context window user-configurable.

Models Settings now provides 16K, 32K, 64K, 128K, and 262K presets plus a
validated custom value from 2,048 through 262,144 tokens. The selected model's
documented context and a hardware-aware recommendation remain visible. Large
values are deliberately labelled as expert or experimental because they can
increase unified-memory use and prompt-processing time.

Changing the context never downloads anything. If the selected model is loading
or loaded, the retained llama.cpp client is unloaded and recreated with the new
value. Header selection, Settings loading, launch-time preload, Send, and the
ready state all use the same persisted context.

The Mac Studio live gate loaded Qwen 3.5 35B-A3B at 262,144 tokens, generated a
response, peaked at 25.70 GiB XCTest RSS, and used no swap. The separate real
Docker Brave regression also continues to pass at 16,384 tokens with the full
`default` profile, multiple MCP rounds, and the correct Argentina–Spain answer.
