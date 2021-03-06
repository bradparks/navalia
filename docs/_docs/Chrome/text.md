---
title: .text
category: Chrome
---

The `text` method returns the inside-text of a DOM node (including its children's text) as a string. It accepts one argument: a css-selector string, and defaults to `body` when none is present.

*JavaScript*
```js
const { Chrome } = require('navalia');
const chrome = new Chrome();

chrome.goto('https://www.google.com')
.then(() => chrome.text('title'))
.then((result) => console.log(res)) // Google
.then(() => chrome.done());
```

*TypeScript*
```ts
import { Chrome } from 'navalia';
const chrome = new Chrome();

async function html() {
  await chrome.goto('https://www.google.com');
  const result = await chrome.text('title');
  console.log(result); // Google
  chrome.done();
}

html();
```
