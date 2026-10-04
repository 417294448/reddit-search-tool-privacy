# Reddit Multi-Language Search Assistant Privacy Policy

Last updated: 2026-10-04

## Overview

Reddit Multi-Language Search Assistant is a browser extension that helps you search and read Reddit in your own language. This privacy policy explains how the extension handles your data.

## Data Collection

The extension does **not** collect, transmit, or store any personal information to servers operated by the developer. There is no analytics, tracking, or advertising. However, two user-initiated features send the input you provide to the LLM endpoint that **you configure yourself**:

- **Generate query**: the native-language text you type is sent to your configured LLM endpoint.
- **Write an English comment**: the comment text you type, together with the context needed to resolve references (the current post title and the parent comment, both truncated), is sent to your configured LLM endpoint.

Your API key is sent only as the `Authorization: Bearer` credential for those requests. The developer never receives, stores, or has access to any of this data.

## Local Storage

- **Settings**: your preferences (LLM endpoint URL, API key, model name, target language, feature toggles, translation color, and sort/time options) are stored locally using Chrome's storage API (`chrome.storage.local`).
- **Search history**: the most recent 20 search entries (the native-language term and the generated query) are stored locally on your device.
- **Translation cache**: title and body/comment translations are cached in memory only, for the current page session.

None of this data is synced to the cloud.

## Data Usage

The extension uses your data only for its core functionality:

- Turning your native-language query into a Reddit search query and opening the results
- Translating English titles, post bodies, and comments in place on Reddit pages
- Converting a native-language comment into English and inserting it into the comment box

Translation of titles, bodies, and comments runs entirely on the browser's built-in on-device translation model. It is free, local, offline, and produces no network transmission and no LLM usage.

## Third-Party Disclosure

The extension does not share any data with third parties. Data is sent only to the LLM endpoint that you configure, and only when you explicitly trigger the related feature. The developer has no access to that transmission, and any handling is governed by the privacy policy of the provider you choose.

## Permissions

The extension requests the following permissions:

- `storage` – To save your settings and search history locally
- `*://*.reddit.com/*` – To read the titles, post bodies, and comments on the current Reddit page and display translations in place
- `*://*/*` (optional) – Requested only when you save a custom LLM endpoint, to call that endpoint; never requested at install time

These permissions are used solely for the core functionality of the extension.

## Remote Code

The extension does not load or execute remote code. All JavaScript is included in the extension package, and no `eval()`, `new Function()`, or dynamic remote imports are used.

## Changes to This Policy

We may update this privacy policy from time to time. Any changes will be reflected in this document, with an updated date at the top.

## Contact

If you have any questions about this privacy policy, please contact us through the extension's GitHub repository.
