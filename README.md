# AmazonCustomerImageEnlarger
A Userscript which enlarges the customer image gallery on amazon.com to make it fill most of the browser's viewport.

## Usage

Install the "TamperMonkey" browser extension, or another Userscript manager of your choice.

Add this Userscript:

```js
// ==UserScript==
// @name         Amazon Customer Image Enlarger
// @namespace    https://github.com/bp2008/AmazonCustomerImageEnlarger
// @version      0.1
// @description  Enlarges the panel for viewing the customer image gallery so that it fills most of the screen.
// @author       bp2008
// @match        https://www.amazon.com/*
// @icon         https://www.google.com/s2/favicons?sz=64&domain=amazon.com
// @grant        GM_addStyle
// ==/UserScript==

(function() {
    'use strict';
    GM_addStyle('.a-popover.a-popover-modal.a-declarative[data-action="a-popover-a11y"] { top: 2vh !important; left: 2vw !important; max-width: 96vw !important; margin: 0 !important; }');
    GM_addStyle('#seeAllImagesContainer,#cr_customers_image_gallery { width: calc(96vw - 50px) !important; height: calc(96vh - 115px) !important; }');
})();
```

## Screenshots

### Before
![AMZ-before-400](https://user-images.githubusercontent.com/5639911/222193806-537006f5-6cd3-47e6-ad44-625e9e029111.png)

### After
![AMZ-after-400](https://user-images.githubusercontent.com/5639911/222193798-0cafa3a6-a8d1-4181-ab38-64fab14b94c5.png)
