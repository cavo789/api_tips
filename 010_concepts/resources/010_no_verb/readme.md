# Don't use verbs in URLs

HTTP has verbs like `GET`, `POST`, `DELETE`, ... so don't use calls like:

* `/articles/gettitle`,
* `/articles/insert`,
* `/articles/1/delete`

But use the adequate HTTP verb:

* `GET /articles/title`,
* `PUT /articles`,
* `DELETE /articles/1`
