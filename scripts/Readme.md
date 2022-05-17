# Scripts used to maintain the documentViewer's use of the PDF.js project

## Using PDF.js as a git submodule

See: [How To Add and Update Git
Submodules](https://devconnected.com/how-to-add-and-update-git-submodules/)

To initially setup the PDF.js git submodule we need to (only once) type:

```
  git submodule add https://github.com/mozilla/pdf.js.git pdfjs
```
and then committe the whole documentVierwer project.


Any time a new copy of the documentViewer project is cloned locally, the
user needs to run the:

```
  ./scripts/pdfjsSetup
```
script *once*.


Whenever an owner of the documentViewer project wants to update the
documentViewer's use of the pdfjs project to a new tag, they need to run
the:

```
  ./scripts/pdfjsUpdate
```
script. This script will list the 10 most recent tags and then ask the
user to specifiy a new tag at the prompt. Once a the pdfjs project has
been updated to a new tag, the documentViewer project as a whole needs to
be committed.
