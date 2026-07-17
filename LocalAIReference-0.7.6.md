# Local AI macOS Reference 0.7.6

This patch removes the remaining round arrow button that could flash while the
Chats sidebar reopened.

The root cause was SwiftUI's automatic `NavigationSplitView` toolbar item.
The sidebar is now an app-owned animated chat column, and both the sidebar and
Models actions live in one stable window-frame overlay. The main window no
longer has native toolbar buttons that macOS can move into an overflow control.

The Mac Studio regression checks both transition directions in English and
German, requires an empty native toolbar throughout the animation, compares the
trailing titlebar pixels, and verifies the fixed controls remain stationary.
The complete 102-test suite passes with zero failures.
