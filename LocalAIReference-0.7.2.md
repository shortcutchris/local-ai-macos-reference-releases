# Local AI macOS Reference 0.7.2

This patch stabilizes the native Chats sidebar transition.

The Models action in the upper-right toolbar now belongs to the persistent chat
detail column rather than the split-view container whose column composition
changes during animation. It remains visible, accessible, and at the same
window-relative position when Chats is open, collapsed, or reopened.

The Mac Studio UI regression exercises all three states, verifies that the
Models action and message composer remain usable, compares the toolbar position
within a two-point tolerance, and retains screenshots for visual review.
