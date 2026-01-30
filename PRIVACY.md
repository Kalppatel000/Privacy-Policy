# Privacy Policy for ServiceNow Markdown Composer

**Last updated:** January 31, 2026

## Overview

ServiceNow Markdown Composer is a browser extension that helps you write formatted comments in ServiceNow using Markdown syntax. This privacy policy explains how the extension handles your data.

## Data Collection

**This extension does NOT collect, transmit, or share any personal data with external servers.**

All data processing happens locally on your device. The extension does not have any analytics, telemetry, or data collection mechanisms.

## Local Storage

The extension stores the following data locally on your device using Chrome's built-in storage APIs:

| Data Type | Purpose | Storage Location |
|-----------|---------|------------------|
| Draft content | Auto-save your work while editing | Chrome local storage |
| User preferences | Remember your sync field selection | Chrome local storage |
| Attachment metadata | Display images in the preview | Chrome local storage |

This data never leaves your browser and is not accessible to anyone except you.

## Permissions Explained

The extension requires the following permissions to function:

### `storage`
- **Purpose:** Save your drafts and preferences locally in Chrome
- **What it does:** Allows the extension to remember your work between sessions
- **Data access:** Only the extension can read/write this data

### `activeTab`
- **Purpose:** Access the current ServiceNow page to inject the markdown composer
- **What it does:** Enables the composer button and editor overlay on ServiceNow pages
- **Data access:** Only reads the current page to find comment fields

### `cookies`
- **Purpose:** Read ServiceNow authentication for uploading attachments
- **What it does:** Uses your existing ServiceNow session to upload images
- **Data access:** Only accesses cookies for ServiceNow domains you're logged into

### Host Permissions (`*.service-now.com`, `*.servicenow.com`)
- **Purpose:** Allow the extension to run on ServiceNow pages
- **What it does:** Enables the content script to inject the composer UI
- **Data access:** Only interacts with ServiceNow pages, no other websites

## Third-Party Services

This extension only communicates with ServiceNow servers that you are already logged into. It does not communicate with any other external services, APIs, or servers.

When you upload an image through the composer, it is uploaded directly to your ServiceNow instance using your existing authentication session.

## Data Security

- All data is stored locally using Chrome's secure storage APIs
- No data is transmitted to external servers
- The extension cannot access data from other websites or extensions
- Your ServiceNow credentials are never stored or accessed by the extension

## Data Retention

- Drafts are automatically deleted after 24 hours of inactivity
- User preferences persist until you clear your browser data
- You can manually clear all extension data through Chrome settings

## Children's Privacy

This extension is designed for business use in ServiceNow environments and is not directed at children under 13 years of age.

## Changes to This Policy

If we make changes to this privacy policy, we will update the "Last updated" date at the top of this document.

## Contact

If you have questions about this privacy policy or the extension's data practices:

- **GitHub Issues:** https://github.com/Kalppatel000/SNComposer/issues
- **Repository:** https://github.com/Kalppatel000/SNComposer

## Open Source

This extension is open source. You can review the complete source code at:
https://github.com/Kalppatel000/SNComposer
