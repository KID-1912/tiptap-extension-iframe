# tiptap-extension-iframe

<h3 align="center">
    A tiptap extension that inserts custom iframe.
</h3>

<br/>

<p align="center">
  <a href="https://www.npmjs.com/package/tiptap-extension-iframe">
    <img
     alt="NPM URL"
     src="https://img.shields.io/badge/npm-tiptapExtensionIframe?logo=npm">
  </a>
  <img
     alt="version"
     src="https://img.shields.io/badge/version-1.0.0-blue">
</p>

---

## Install

```shell
npm install tiptap-extension-iframe -S
```

## Usage

```js
import Iframe from "tiptap-extension-iframe";

const editor = new Editor({
  element: document.querySelector(".editor"),
  extensions: [StarterKit, Iframe],
});

editor
  .chain()
  .focus()
  .setParagraph()
  .setIframe({
    src: `http://v.qq.com/txp/iframe/player.html?vid=${videoId}`,
    HTMLAttributes: {
      class: "video_iframe",
      style: `height: 325px;border-radius: 4px;pointer-events: none;`,
    },
  })
  .run();
```

## Options

You can configure common iframe HTML attributes via the `HTMLAttributes` options

```js
  extensions: [
    StarterKit,
    Iframe.configure({
      HTMLAttributes: { frameborder: 0 }, // default HTMLAttributes
    }),
  ],
```

## Relations

**@tiptap/extension-image:** https://github.com/ueberdosis/tiptap/tree/develop/packages/extension-image

**tiptap-appmsg-editor:** https://github.com/KID-1912/tiptap-appmsg-editor