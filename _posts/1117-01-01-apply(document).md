---
category: reference
---


---------------

Applies the patch to the given document and returns the result. May also mutate the document!

  * document  - The document to operate against. May be mutated.

Example:

    javascript
    patched = mypatch.apply(mydoc);


Returns the patched document.

Throws:

   * PatchApplyError if the patch could not apply against the given document

