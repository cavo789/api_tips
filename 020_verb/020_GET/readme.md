# GET

Return a resource (can be a collection or just one).

Return all employees:

```bash
curl -X GET http://localhost:3000/employees
   -H "Accept: application/json" 
```

Return the employee #1:

```bash
curl -X GET http://localhost:3000/employees/1
   -H "Accept: application/json" 
```
