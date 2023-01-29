# Top Level

> [https://jsonapi.org/format/#document-top-level](https://jsonapi.org/format/#document-top-level)

A document MUST contain at least one of the following top-level members:

* `data`: the document's *primary data*.
* `errors`: an array of error objects.
* `meta`: a meta object that contains non-standard meta-information.

But never both `data` and `errors`

The document's *primary data* is a representation of the resource or collection of resources targeted by a request. 

`data` can be an array or not:

```json
{
  "data": {
    [
        "key1": "value1",
        "key2": "value2",
        // ...
    ],
    [
        // ...
    ]
  }
}
```

or, if just one record, directly:

```json
{
  "data": {
    "key1": "value1",
    "key2": "value2",
    // ...
  }
}
```
