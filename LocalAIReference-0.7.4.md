# Local AI macOS Reference 0.7.4

This patch removes the extra round button that could flash beside Models at the
end of the Chats sidebar reopening animation.

The native titlebar accessory now uses a unified compact macOS toolbar layout.
Models stays fixed at the upper-right while AppKit no longer inserts its
temporary toolbar-overflow control during the transition.

The Mac Studio UI regression checks both English and German system labels for
that overflow control throughout sidebar collapse and reopening, in addition to
the existing button-position and final-state screenshot checks.
