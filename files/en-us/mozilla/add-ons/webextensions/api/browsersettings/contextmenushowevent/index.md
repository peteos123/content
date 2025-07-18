---
title: browserSettings.contextMenuShowEvent
slug: Mozilla/Add-ons/WebExtensions/API/browserSettings/contextMenuShowEvent
page-type: webextension-api-property
browser-compat: webextensions.api.browserSettings.contextMenuShowEvent
sidebar: addonsidebar
---

A {{WebExtAPIRef("types.BrowserSetting", "BrowserSetting")}} object which determines whether the browser's context menu is shown on the mouseup event or on the mousedown event.

Its underlying value is a string that may be either "mouseup" or "mousedown".

The default value is "mouseup" on Windows, and "mousedown" on macOS and Linux. Assigning to it on Windows has no effect - the setting is only designed to allow the context menu to be opened on mouseup instead of mousedown, not the inverse.

## Examples

Set the setting to "mouseup":

```js
function logResult(result) {
  console.log(`Setting was modified: ${result}`);
}

browser.browserSettings.contextMenuShowEvent
  .set({ value: "mouseup" })
  .then(logResult);
```

{{WebExtExamples}}

## Browser compatibility

{{Compat}}
