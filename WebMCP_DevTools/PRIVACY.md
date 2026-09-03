# Privacy Policy — WebMCP DevTools

**Last updated: September 3, 2026**

This privacy policy applies to the Chrome extension **WebMCP DevTools**. It explains what data the extension accesses, how that data is used, and where it is stored.

## Overview

WebMCP DevTools is a developer tool that helps inspect, test, and monitor WebMCP tools registered on web pages via `document.modelContext` (with fallback to `navigator.modelContext`).

**WebMCP DevTools does not collect, store, or transmit any personal data to our servers.**

Specifically:

- **No analytics** — We do not use any analytics or tracking services
- **No browsing history collection** — We do not collect, sell, or share browsing history
- **No first-party servers** — The extension does not operate a backend that receives user data from the extension UI

## Data Collection

This extension does **not** collect personal information, account credentials, payment data, or health data.

Page content and WebMCP tool definitions are accessed **only** to provide the extension’s debugging features on the page you currently have open. That data stays in your browser unless you explicitly use an optional feature that sends data to a provider you configured (see AI Assistant below).

## Permissions Explained

The extension uses the following Chrome APIs for its core functionality:

- **`sidePanel`** — To display the developer tool UI in Chrome’s Side Panel, where you inspect tools, schemas, execution results, timelines, and snapshots
- **`activeTab`** — To communicate with the currently active tab so the extension can detect and execute WebMCP tools on that page
- **`scripting`** — To inject content scripts that detect WebMCP tool registrations via `document.modelContext` / `navigator.modelContext`
- **`storage`** — To save local preferences, snapshots, execution history, and optional AI configuration using `chrome.storage.local`
- **`alarms`** — To run lightweight periodic keepalive tasks in the service worker so debugging sessions remain reliable while the side panel is in use
- **Host access (`<all_urls>`)** — WebMCP tools can appear on any website. This permission lets the extension detect tools on the page you navigate to. The extension does not collect or transmit browsing data to the developer

## Local Storage

The following data may be stored locally in your browser profile via `chrome.storage.local`:

- Theme preference (System / Light / Dark)
- Language preference (English / Chinese)
- Tool definition snapshots and execution history
- Optional site profiles and generated tool definitions
- Optional AI assistant configuration (provider, model, endpoint, API key)

This data is stored only on your device. It is never transmitted to the WebMCP DevTools developer.

## Page and Tool Data

When you open the side panel on a page, the extension may read:

- Registered WebMCP tool names, descriptions, schemas, and execution results
- Declarative WebMCP form attributes on the page
- Page metadata, visible text, tables, forms, and links **only when you explicitly use page-scan or content-reading features**

This information is displayed in the side panel for debugging. It is discarded from memory when you close the panel or navigate away, except for items you explicitly save (snapshots, history, or site profiles).

## AI Assistant (Optional)

The built-in AI assistant is optional and requires an API key that **you** provide.

If you use it:

- Your API key is stored only in `chrome.storage.local` on your device
- Chat messages and relevant tool/page context are sent **only** to the AI provider endpoint you configured (for example Gemini, OpenAI, Claude, DeepSeek, or a custom endpoint)
- Data is sent **only** when you submit a message in the AI panel
- The extension does not route this traffic through a developer-operated server
- The AI provider’s own privacy policy applies to data processed by their API

## Third-Party Services

This extension does **not** use third-party analytics, advertising, or tracking SDKs.

Optional network requests occur only when:

- You use the AI assistant, in which case requests go directly to the endpoint you configured

## Changes to This Policy

If this privacy policy changes, the “Last updated” date at the top of this document will be updated.

## Contact

If you have questions about this privacy policy, please open an issue on the [GitHub repository](https://github.com/2019-02-18/WebMCP-DevTools/issues).
