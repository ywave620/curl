---
c: Copyright (C) Daniel Stenberg, <daniel@haxx.se>, et al.
SPDX-License-Identifier: curl
Long: preserve-connection
Help: Keep connection alive after request completes
Category: connection
Added: 8.16.0
Multi: boolean
See-also:
  - connect-timeout
  - keepalive
  - no-keepalive
Example:
  - --preserve-connection $URL
---

# `--preserve-connection`

Instructs curl to preserve the connection after the request completes instead
of exiting immediately. This keeps the connection alive and curl will wait for
user interruption (Ctrl+C) before exiting.

This can be useful for debugging connection issues, testing connection 
persistence, or keeping connections warm for subsequent requests.

When this option is used, curl will display a message indicating that the
connection is preserved and will instruct the user how to exit.