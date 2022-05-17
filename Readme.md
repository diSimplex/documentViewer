# Document/Comment Viewer

A PDF document viewer with the ability to synchronise a collection of
static comments with individual pages/sections of the viewed PDF document.

This diSimplex documentViewer is based upon the [Mozilla
PDF.js](https://github.com/mozilla/pdf.js) tool.

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

## Building from source

Since PDF.js is embedded as a [git
submodule](https://git-scm.com/docs/git-submodule) ([see
also](https://git-scm.com/book/en/v2/Git-Tools-Submodules)) anyone using
the documentViewer from source code needs to make use of the
`./scripts/pdfjsCloneSetup` script to ensure the correct copy of PDF.js is
installed. See the `scripts/Readme.md` for details.

Once the PDF.js source code has been locally embedded in the
documentViewer project, you can use the "standard" PDF.js gulp commands:

- **`gulp generic`** command to compile the source - **`gulp server`**
command to run a local test (note the Javascript and CSS files are *not*
optimised or minified, so loading this local test can be slow).

## Licenses

Unless otherwise noted all software in the diSimplex documentViewer
project is copyright 2022 by Perceptisys Ltd (Stephen Gaito) and
distributed using the [Apache 2.0 License
](http://www.apache.org/licenses/LICENSE-2.0).

```
Copyright 2022 Perceptisys Ltd (Stephen Gaito)

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

Since the diSimplex documentViewer project is a derivative of the Mozilla
PDF.js project, *some* files in the documentViewer project have been
modified from corresponding files in the PDF.js project. Any modifications
are noted at the top of the modified files.

Both the documentViewer and PDF.js projects are licensed using the same
Apache 2.0 License.

The documentViewer project embeds the *whole* of the PDF.js project as a
[git submodule](https://git-scm.com/docs/git-submodule) ([see
also](https://git-scm.com/book/en/v2/Git-Tools-Submodules)). All of the
unmodified PDF.js files used to build the documentViewer, are used via
*nix symbolic links.

Note that the documentViewer `package.json` file has been taken from the
PDF.js v2.14.305 on 2022/05/17. (Unfortunately JSON does not allow
comments so it is the only modified file without a License declaration).
