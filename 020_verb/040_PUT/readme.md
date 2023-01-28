# PUT

**Means `UPDATE` in `CRUD`, when you'll update every fields**  

Using `PUT` you'll update an existing resource.

```bash
curl -X PUT http://localhost:3000/articles/15
     -d '{"title":"Introduction to API", "author":"John"}'
```

Consider using `PUT` only when you'll update every information's of the resource. If you wish to update just a few ones (partial content), Consider using `PATCH`.

`PUT` is idempotent since running the same update won't have other effects on the server. You can update once, five or one thousand times the title of the article #15, the result will always be the same.

If successfully updated will return the HTTP status code `200` (OK) or `204` (No Content) if nothing is updated. If successfully created will return the HTTP status code `201` (CREATED) (like when using the `POST` verb).

Note: depending on the API developer, updating an inexisting resource can return an error ('Resource #15 do not exist') or the developer can decide to create it (and thus do the same thing as the `PUT` verb). This is indeed possible since `PUT` is used for full content: you've sent to the server every possible field so it's possible to create it.
