# Local AI macOS Reference 0.7.3

This patch removes the final snap from the Chats sidebar transition.

The Models button in the upper-right corner is now a native trailing macOS
titlebar accessory. Its position is independent of the split-view hierarchy
that animates when the Chats sidebar opens or closes, so it no longer jumps
left immediately before the sidebar finishes reopening.

The Mac Studio regression samples the button position throughout both
directions of the transition, allows at most two points of movement, and covers
open, collapsed, and reopened states in both English and German. Screenshots
are retained for visual review.
