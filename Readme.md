# Document/Comment Viewer

A PDF document viewer with the ability to synchronise a collection of
static comments with individual pages/sections of the viewed PDF document.

We will use the [Mozilla PDF.js](https://github.com/mozilla/pdf.js) tool.

In particular we will modify the
[viewer.html](https://github.com/mozilla/pdf.js/blob/master/web/viewer.html)
page to add a comments sidebar on the right similar to the organisation
sidebar on the left. We will also provide a hide-able comment entry footer
below the PDF canvas, which can be used to add new comments.

## Resources

- [mozilla/pdf.js](https://github.com/mozilla/pdf.js)

- [online demo](https://mozilla.github.io/pdf.js/web/viewer.html)

- [How to Create a JavaScript PDF
  Viewer](https://code.tutsplus.com/tutorials/how-to-create-a-pdf-viewer-in-javascript--cms-32505)

- [Add HTML/CSS overlays by text location on pdf document when rendering
  in pdf.js
  viewer](https://stackoverflow.com/questions/27830725/add-html-css-overlays-by-text-location-on-pdf-document-when-rendering-in-pdf-js)

- [W3Schools: How TO -
  Overlay](https://www.w3schools.com/howto/howto_css_overlay.asp)

## Installation

Our documentViewer is built upon the [Mozilla
PDF.js](https://mozilla.github.io/pdf.js/) `web/viewer.html`. However we
make a number of important changes to this pre-existing code. To do this
*cleanly* we *should* install PDF.js as a standard `npm` module.
Unfortunately for a number of reasons this does not work in our
environment. So, instead, we manually install the PDF.js source code into
the local `node_modules` directly using the `./scripts/installPDFjs` bash
script.

To fully install documentViewer from source, in the bottom of the
documentViewer git repository, type:

```
npm install
./scripts/installPDFjs
```