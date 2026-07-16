# Local AI macOS Reference 0.5.2

Assistant answers now render Markdown instead of exposing raw markers. Headings, emphasis, links, nested ordered and unordered lists, quotes, and fenced code receive native macOS formatting while remaining selectable.

Qwen thinking output is now separated from the final answer even when the model's chat template pre-fills the opening `<think>` marker and the generated stream contains only `</think>`. The localized Reasoning/Überlegungen section is briefly visible during generation, collapses automatically after 2.5 seconds or when the answer starts, and can be reopened. Reasoning is excluded from Copy and subsequent conversation context.

The text-model pill in the chat header is now a quick picker similar to LM Studio. It lists only already installed and verified GGUF models; choosing one selects and loads it into memory. The same menu can cancel loading, unload the current model, or open model management. Downloads and deletion remain separate in Settings, and switching is disabled during an active request.

Inference remains embedded and local. This update adds no account, daemon, implicit model download, or content network request.
