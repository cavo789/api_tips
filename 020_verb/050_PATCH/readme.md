# PATCH

**Means `UPDATE` in `CRUD`, when you'll update just a few fields**  

See `PUT` when you'll update the entire resource.

`PATCH` is to be used when the update is partial like updating, just, one column: `curl -X PATCH http://localhost:3000/employee/1 -d '{"firstname": "Christophe"}'` will, only, update first name.

If successfully updated will return the HTTP status code `200` (OK) or `204` (No Content) if nothing is updated. If successfully created will return the HTTP status code `201` (CREATED) (like when using the `POST` verb).

`PATCH` on an inexisting resource will return an error while, perhaps, `PUT` will create the resource. If's then safer to use `PATCH` and not `PUT` when updating partial content.  

It's indeed impossible to create a new record with `PATCH` since the request just mention a few information's, not all.
