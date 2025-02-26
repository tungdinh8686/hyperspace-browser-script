# Installation Instructions

Follow these steps to install and set up the Tampermonkey script for your browser.

---

## 1. Install Tampermonkey

- Install the [Tampermonkey extension](https://www.tampermonkey.net/) for your browser:
  - **[Chrome](https://chromewebstore.google.com/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo)**
  - **[Firefox](https://addons.mozilla.org/en-US/firefox/addon/tampermonkey/)**
- Click **"Add to Chrome"** or **"Add to Firefox"** and confirm the installation.

---

## 2. Create a New Script

1. Click the **Tampermonkey icon** in your browser’s toolbar (it looks like a little monkey).
2. Select **"Dashboard"** from the dropdown menu.
3. In the Dashboard, click the **"+"** button to open a new script editor.

---

## 3. Add or Download the Script
1. Download the script if you want [HyperSpace_AutoConnect]( or
2. Copy the following script code:
   
```javascript
   // ==UserScript==
   // @name         Hyperspace Node Auto-Reconnect
   // @match        https://node.hyper.space/*
   // @grant        none
   // ==/UserScript==

   (function() {
       'use strict';
       setInterval(() => {
           const toggleButton = document.querySelector('button[role="switch"]');
           if (toggleButton && toggleButton.getAttribute('aria-checked') === 'false') {
               toggleButton.click();
               console.log('Node turned back on!');
           }
       }, 10000); // Every 5 minutes
   })();

