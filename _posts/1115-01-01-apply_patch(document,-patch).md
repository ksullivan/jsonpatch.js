---
category: reference
---

A shortcut to apply a patch given as an Array or as a JSON String (see the [draft JSONPatch spec][#jsonpatch] for the patch format) to a document. May (and usually does)  mutate the given document.

   * document - The document to operate against. May be mutated.
   * patch - The patch document as a JS Array of operations or as a JSON String representing the same (the latter requires JSON support in your browser or the inclusion of the JSON2 library or similar)

Example:

    javascript
    mydoc = {
      "baz": "qux",
      "foo": "bar"
    };
    thepatch = [
      { "replace": "/baz", "value": "boo" }
    ]
    patcheddoc = jsonpatch.apply_patch(mydoc, thepatch);
    // patcheddoc now equals {"baz": "boo", "foo": "bar"}}


[#jsonpatch]: http://tools.ietf.org/html/draft-pbryan-json-patch-01

Throws:

   * InvalidPatch if the patch is invalid
   * PatchApplyError if the patch could not apply against the given document

