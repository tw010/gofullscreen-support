---
layout: default
title: Privacy Policy - GoFullScreen
---

# Privacy Policy: GoFullScreen

_Last updated: 2026-08-19_

GoFullScreen is a Google Chrome extension that captures a complete,
full-page screenshot of the webpage you are currently viewing, with a single
click. This policy explains what data the extension processes, where it is
processed, and why.

## Summary

- All processing happens locally inside your browser on your device.
- No screenshot, webpage content, URL, or setting is uploaded or sent to the
  developer or any third party.
- The extension has no backend and makes no remote data requests.
- The developer does not receive, store, or have access to screenshots,
  webpage content, browsing history, or URLs.
- There are no accounts, analytics, advertisements, tracking, or data sales.

## Data GoFullScreen processes

When you click the GoFullScreen toolbar button, the extension:

1. Reads the layout and visible pixels of the active tab only.
2. Temporarily scrolls that tab to capture each section of the page.
3. Combines the captured sections into a single image inside your browser.
4. Stores that image temporarily in local IndexedDB storage so it can be
   displayed in the bundled viewer.
5. Lets you copy, annotate, crop, download, split, or export the image as a
   PDF.

The extension also reads temporary page-layout information such as element
dimensions, scroll positions, visibility, and fixed or sticky positioning.
This information is used only to select and scroll the capture area. It is not
transmitted or stored after capture.

The captured pixels can contain any information visibly shown on the page the
user chooses to capture. Depending on the page, this may include website
content, personal communications, form content, names, account information,
or other sensitive information. GoFullScreen does not separately extract,
classify, or inspect that information. It handles it only as part of the
user-requested screenshot.

GoFullScreen stores preferences with `chrome.storage.local`, including capture
mode, image format and quality, filename prefix, download behavior, image-part
settings, clipboard resizing, and local counters used to limit the frequency
of the optional rating prompt. These settings stay on the device and are never
transmitted.

Under the Chrome Web Store User Data Policy, website content and screen
captures can be considered user data even when processed only locally. This
policy applies to that local processing even though nothing is transmitted.

## What GoFullScreen does not do

GoFullScreen does not:

- Upload screenshots, webpage content, HTML, settings, or URLs.
- Store screenshots outside the user's device.
- Give the developer or anyone else access to screenshots or visited pages.
- Collect or transmit browsing history.
- Run analytics about websites the user visits.
- Track users across websites or sessions.
- Show advertisements.
- Sell, rent, or share data with third parties.
- Use an external API or remote server for capture, editing, or export.
- Require an account or sign-in.

## Where processing happens

All processing happens on the user's device inside the Chrome extension
sandbox:

- Screenshot capture: Chrome's built-in `tabs.captureVisibleTab` API.
- Scrolling and measurement: a script injected only into the tab selected by
  the user and only for the duration of the capture.
- Image stitching: an in-memory canvas in the extension service worker.
- Temporary image storage: local IndexedDB. Older screenshot records are
  cleared whenever a new completed screenshot is stored.
- Preferences and local counters: `chrome.storage.local` on the device.
- Display, editing, copying, and downloading: pages bundled with the extension.

No part of this pipeline sends data to a server operated by the developer or
any third party.

## Data retention

The most recent screenshot is kept in local IndexedDB only so the viewer can
display it. Older screenshot records are removed when a new screenshot is
stored. Preferences and local counters remain in `chrome.storage.local` until
the user resets them, clears the extension data, or uninstalls GoFullScreen.
Nothing is retained by the developer because the developer never receives it.

## Permissions

GoFullScreen requests the minimum permissions required for its features:

- **`activeTab`**: temporarily grants access to the tab on which the user
  invokes GoFullScreen. It does not provide standing access to browsing.
- **`scripting`**: runs the scrolling and measurement logic on that same tab
  after the user starts a capture.
- **`storage`**: stores extension settings locally on the device.
- **`downloads` (optional)**: requested only if the user enables "Ask where
  to save each screenshot" so Chrome can display its native Save As dialog.
  The permission is removed again when that setting is disabled.

GoFullScreen does not request host permissions, `<all_urls>`, browsing history,
cookies, or access to clipboard contents.

## Limited Use disclosure

GoFullScreen's use of information follows the Chrome Web Store User Data
Policy and Limited Use requirements:

- Captured pixels are used only to provide the disclosed screenshot feature.
- No data is transferred to a third party.
- No data is used for advertising.
- No human reads or reviews screenshots or browsing content because the data
  never leaves the device.

## External navigation

External links open only after the user clicks them. They can open the
GoFullScreen rating page in the Chrome Web Store or GoFullScreen's support and
capture-test pages. These links do not attach screenshot, webpage, URL, or
settings data.

## Changes to this policy

If GoFullScreen changes how it handles data, this policy, the Chrome Web Store
listing, and any required in-product disclosures will be updated before the
change takes effect.

## Contact and support

For privacy questions, bug reports, or support, open a request in the
[GoFullScreen support repository](https://github.com/tw010/gofullscreen-support/issues/new).
