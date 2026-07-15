# Local AI macOS Reference 0.3.1

This maintenance release makes application updates and ordinary quitting graceful while a local GGUF model is loaded. The app now delays termination long enough to cancel active generation or transcription work, waits for those operations to finish, unloads the shared model session, and releases its Metal resources before Sparkle replaces the bundle or macOS exits the process. This prevents the crash report that could appear after an otherwise successful update.
