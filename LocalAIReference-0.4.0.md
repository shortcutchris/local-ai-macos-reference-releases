# Local AI macOS Reference 0.4.0

Whisper can now be prepared before dictation. Click the speech-model status pill to load, cancel, or unload the selected installed model, or enable the new opt-in launch preload in Settings. The app shows the real indeterminate Core ML loading state, explains the first-run delay and memory cost, and never downloads a model as a side effect of preload.

Once loaded, the shared WhisperKit runtime is reused across recordings instead of rebuilding the speech pipeline for every transcription. Recording still produces editable composer text only after a complete local transcript, and cancellation, model changes, app termination, and Sparkle updates cleanly stop work and release the retained speech runtime.
