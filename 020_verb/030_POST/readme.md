# POST

**Means `CREATE` in `CRUD`**

Using `POST` you'll create a new resource. Calling `POST` five times for the same "new" employee will thus create five new employees. `POST` is **not** idempotent meaning calling it more than once will return every time a new resource (like the new employee id)

```bash
curl -X POST http://localhost:3000/employees
   -d '{"firstname":"christophe",...}'
```

The example here above will create a new employee, the server will return the HTTP status code `201` (CREATED) and, probably, also return a location-header with a link, like `http://localhost:3000/employees/999` i.e. the link to the newly created employee.
