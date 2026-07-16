# Local AI macOS Reference 0.5.3

The speech-model pill now works like the text-model picker. It lists installed Whisper models, and choosing one selects and loads it into the shared local runtime. The same menu can switch models, cancel loading, unload the current model, or open model management.

“Manage models…” now reliably opens Settings directly on the Models tab, even when another Settings tab was selected previously. Settings labels on-disk selection as “Select”/“Auswählen” so it remains distinct from the separate action that loads a model into memory.

Whisper switching no longer races with an open Settings window, and deleting the selected speech model unloads its retained runtime first. Both header pickers remain disabled while foreground work owns the relevant runtime.

All model loading and inference remain embedded and local. The pickers list only installed models and never start a download or catalog network request.
