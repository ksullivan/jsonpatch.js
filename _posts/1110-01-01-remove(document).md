---
category: reference
---

Takes a JSON document and removes the value pointed to.
It is an error to attempt to remove a value that doesn't exist.

   * document - The document to operate against. May be mutated.

Example:

    javascript
    var doc = new JSONPointer("/obj/old").remove({obj: {old: "string"}});
    // doc now equals {obj: {}}

Returns the updated doc (the value passed in may also have been mutated)

