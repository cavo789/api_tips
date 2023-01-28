# Top Level

> [https://jsonapi.org/format/#document-top-level](https://jsonapi.org/format/#document-top-level)

A document MUST contain at least one of the following top-level members:

* `data`: the document's *primary data*.
* `errors`: an array of error objects.
* `meta`: a meta object that contains non-standard meta-information.

But never both `data` and `errors`
