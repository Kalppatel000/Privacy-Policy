# Privacy Policy — ServiceNow Markdown Composer

**Last updated:** April 2026

---

## Overview

ServiceNow Markdown Composer ("the Extension") is a Chrome browser extension that provides a markdown editor overlay for writing formatted comments in ServiceNow. This policy explains exactly what data the Extension collects, where it goes, and what stays on your device.

---

## What Data Is Collected

### 1. Usage Analytics (Google Analytics 4)

The Extension sends anonymous usage events to Google Analytics 4 (GA4) to help the developer understand how features are used. These events include:

- Composer opened or closed
- Content inserted into a ServiceNow field
- Content copied to clipboard
- Keyboard shortcuts used
- Templates used
- Spell check enabled or disabled
- Errors encountered

**What is NOT sent:** The content you write, your work notes, case data, or any ServiceNow record information.

**User identifier:** Each event includes your ServiceNow username (e.g. `kalp.patel`) as a GA4 user ID so that usage can be understood on a per-user basis. This data is sent to Google Analytics and governed by Google's privacy policy.

Events are sent to: `https://www.google-analytics.com`

---

### 2. ServiceNow User Information

When you open the composer, the Extension reads the following information from your ServiceNow session:

- **Display name and username** — used to personalise your signature and for analytics (see above)
- **Employee number** — checked once to determine whether to show the "Ask Claude" button (contractors with an employee number beginning with "C" do not see this button). The result is cached locally and not sent anywhere.
- **CSRF token** — used to authenticate API calls made to your ServiceNow instance on your behalf (e.g. KB article lookups, case attachment)

This information is read from your existing authenticated ServiceNow session. No credentials are stored.

---

### 3. Data Stored Locally on Your Device

The following data is stored **only on your device** using Chrome's local storage and IndexedDB. It is never transmitted to any external server.

| Data | Storage | Encryption |
|------|---------|------------|
| Draft content (auto-saved while writing) | IndexedDB | AES-256-GCM |
| Custom dictionary words | IndexedDB | AES-256-GCM |
| Message templates | Chrome storage | AES-256-GCM |
| Your signature text | Chrome storage | AES-256-GCM |
| Claude API key (if configured) | IndexedDB | AES-256-GCM |
| Extension preferences and settings | Chrome storage | None |

Encryption keys are non-extractable and stored in IndexedDB. Draft content is automatically deleted after 12–24 hours or when content is submitted.

---

### 4. Anthropic API ("Ask Claude" feature)

If you configure a personal Claude API key and use the "Ask Claude" feature, the text you send in that conversation is transmitted to Anthropic's API at `https://api.anthropic.com`. This uses **your own API key** and is subject to [Anthropic's Privacy Policy](https://www.anthropic.com/privacy).

- The Extension itself does not store chat history beyond the current session
- Chat history is cleared when you close the composer
- No conversation data is sent to the Extension developer

---

## What the Extension Can Access

The Extension runs only on ServiceNow domains:
- `*.service-now.com`
- `*.servicenow.com`
- `*.servicenowcloud.com`

It does not activate on any other website.

Within ServiceNow pages, the Extension reads the current page's URL, session context, and CSRF token in order to function. It does not read, copy, or transmit the content of your ServiceNow records to any external service (other than Anthropic, when you explicitly use Ask Claude).

---

## Data Sharing

The Extension shares data with the following third parties:

| Party | What is shared | Purpose |
|-------|---------------|---------|
| Google Analytics | Usage events + SN username | Product analytics |
| Anthropic | Your chat messages (Ask Claude only) | AI responses |

No data is sold, rented, or shared with any other third party.

---

## Your Controls

- **Analytics opt-out:** You can disable GA4 analytics collection by turning the extension off in Chrome settings.
- **Local data deletion:** You can clear all locally stored data (drafts, dictionary, settings) by removing the extension from Chrome (`chrome://extensions` → Remove).
- **API key:** You can remove your Claude API key at any time from the extension popup.
- **Custom dictionary:** Words added to your personal dictionary can be removed individually from the popup settings.

---

## Children's Privacy

This Extension is intended for use by professional employees in a workplace context. It is not directed at children under 13.

---

## Changes to This Policy

If the data practices described here change materially, the version date at the top of this document will be updated. Continued use of the Extension after a policy update constitutes acceptance of the revised policy.

---

## Contact

If you have questions about this privacy policy or the Extension's data practices, please open an issue at:
**https://github.com/Kalppatel000/SNComposer**
