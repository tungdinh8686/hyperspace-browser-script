# Installation Instructions

Follow these steps to install and set up the Tampermonkey script for your browser.

---

## 1. Install Tampermonkey

- Install the [Tampermonkey extension](https://www.tampermonkey.net/) for your browser:
  - **[Chrome](https://chromewebstore.google.com/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo)**
  - **[Firefox](https://addons.mozilla.org/en-US/firefox/addon/tampermonkey/)**
- Click **"Add to Chrome"** or **"Add to Firefox"** and confirm the installation.
- Turn on Developer Mode at chrome://extensions/
---

## 2. Create a New Script

1. Click the **Tampermonkey icon** in your browser’s toolbar (it looks like a little monkey).
2. Select **"Dashboard"** from the dropdown menu.
3. In the Dashboard, click the **"+"** button to open a new script editor.

---

## 3. Add or Download the Script
1. Download the script if you want [HyperSpace_AutoConnect](https://github.com/tungdinh8686/hyperspace-browerser-script/blob/main/hyperspacebrowsernode.js)
2. or just Copy the following script code:
   
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
       }, 60000); // Every 1 minutes
   })();
```
## 4. Enable the Script
- Ensure the script is toggled on in the Tampermonkey dashboard.

- Look for the switch next to the script name and make sure it's in the "on" position then F5 to refresh

## 5. If this helpful you can send me a cup of coffe
donation:0x3183757e70b1454528712729D42A3058CEb13941
