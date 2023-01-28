# HEAD

`HEAD` has to be used to retrieve information's about the resource like f.i. the number of records in the resource (number of books, articles, ...) or to check if a resource exists.

For instance, imagine a resource called `countrylanguage`, we can verify if there are records for `countrycode=BEL`:

```bash
❯ curl --head http://localhost:3000/countrylanguage\?countrycode\=eq.BEL
HTTP/1.1 200 OK
Date: Sat, 28 Jan 2023 20:17:08 GMT
Server: postgrest/10.1.1
Content-Range: 0-5/*
Content-Location: /countrylanguage?countrycode=eq.BEL
Content-Type: application/json; charset=utf-8
```

If we get a HTTP return code `200`, we can run a `GET` action to get records:

```bash
❯ curl http://localhost:3000/countrylanguage\?countrycode\=eq.BEL | jq
```

`HEAD` can thus be used to get meta data about a resource.
