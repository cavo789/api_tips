# Returning an error 

> [https://jsonapi.org/format/#document-top-level](https://jsonapi.org/format/#document-top-level)

> [https://jsonapi.org/format/#error-objects](https://jsonapi.org/format/#error-objects)

As described in [Top Level items](https://jsonapi.org/format/#document-top-level), errors should be put as a top level node and use the plural form:

```json
"errors": [
    [ ... ]
]
```

Prefer to use HTTP status code `400 Bad Request` when the call was incorrect like an unknown value is used for a parameter (like `&lang=it` when Italian isn't supported). Use code `500 Internal Server Error` when the server has returned an error.

`errors` has to be an array so we can return more than once and should contain at least one of these keys (*not exhaustive*):

* `status`: the HTTP status code applicable to this problem, expressed as a string value. This SHOULD be provided.
* `code`: an application-specific error code, expressed as a string value.
* `title`: a short, human-readable summary of the problem that SHOULD NOT change from occurrence to occurrence of the problem, except for purposes of localization.
* `parameter`: a string indicating which URI query parameter caused the error.

```json
"errors": [
    [ 
        "status": 400,
        "code": "ERR_INVALID_VIEW",
        "title": "Language code 'it' is not supported",
        "parameter": "lang"
    ],
    [ ... ]
]
```
