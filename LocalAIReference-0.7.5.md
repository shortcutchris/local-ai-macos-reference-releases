# Local AI macOS Reference 0.7.5

This patch removes the remaining round arrow button that could flash beside
Models as the Chats sidebar finished reopening.

Models now lives in a dedicated native window-frame overlay at its familiar
upper-right position. It is outside both the animated Chats split view and
AppKit's toolbar/titlebar-accessory layout. The native toolbar owns only the
sidebar toggle, so macOS has no second item to move into its temporary overflow
control.

The Mac Studio UI regression now checks the complete toolbar button set
throughout both transition directions in English and German. Any extra,
unlabeled, or differently localized transient button fails the release gate.
