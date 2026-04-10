# Privacy Policy — Markdown Runner

**Last updated:** April 2026

## Overview

Markdown Runner is a browser extension that enhances code blocks on web pages. This policy explains how the extension handles user data.

## Data Collection

**Markdown Runner does not collect any personal data.**

The extension does not:
- Collect or store personal information
- Track browsing history or behavior
- Use cookies for tracking
- Transmit data to external servers
- Use analytics, telemetry, or crash reporting
- Access passwords, form data, or financial information

## Data Storage

The extension stores only user preferences (feature toggles, theme setting, language, folding threshold, execution timeout, and site list) using the Chrome Storage Sync API. This data:
- Is stored locally and synced through the user's Google account
- Contains no personal information
- Can be cleared by uninstalling the extension

## Page Content Access

The extension reads the DOM of web pages to detect code blocks (`<pre>` and `<code>` elements). This processing:
- Happens entirely in the user's browser
- Does not extract, store, or transmit page content
- Only modifies the visual presentation of code blocks

## Network Requests

The extension makes no network requests except:
- **Mermaid.js library:** When the user explicitly clicks a "Render" button on a Mermaid code block, the extension loads the Mermaid rendering library from `cdn.jsdelivr.net`. No user data or diagram content is sent to this CDN.

## Permissions

See the [Store Listing](STORE_LISTING.md) for detailed permission justifications.

## Changes

If this policy changes, the updated version will be published alongside the extension update.

## Contact

For questions about this policy, please open an issue at:
https://github.com/2019-02-18/markdown-runner/issues
