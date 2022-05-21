# Tasks to do....

- Add comments pane (to the right of the main document -- balancing the
  table of contents pane on the left).

- Track page-goto / scrolling in the comments pane

    - use the EventBus in the code associated with the comments pane, to
      listen for page change and scroll events.

- Add comments entry pane below the main document (hidden most of the
  time).

- Over ride the PDF "FIT" behaviour of the page-goto system. (Do this by
  monkey patching? OR using a Pull Request on the main PDF.js?)

- Allow "external" url-gotos (at least to a list of acceptable domains)
  using monkey-patches.

**To do the above** we wrap the existing app with our own code.

## Changes required:

1. take control of viewer.html and add additional divs.

2. take control of viewer.js and add additional elements corresponding to
   the new divs.

3. create a new dviewer.css and add it *after* viewer.css in the header of
   viewer.html so that the dviewer.css changes take precedent over any
   specified in the viewer.css.

4. create a new dapp.js which subclasses the classes in app.js to add the
   new diSimplex comment functionality.

5. use the new classes from dapp.js in the viewer.js

6. create a new monkey_patch.js which (temporarily?) holds any required
   monkey-patches to the existing PDF.js code base.

7. require the monkey_patch.js in either viewer.js or viewer.html *after*
   all PDF.js code has been loaded.

8. take control of the app_options.js to ensure any diSimplex based
   options are honoured.

## Checking tools

We require tools (bash/diff scripts) which can be run each time the PDF.js
code base is updated to verify that the small changes we make to the
following files will not be broken:

- viewer.html
- viewer.js
- app_options.js
