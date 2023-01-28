# Send the HTTP Accept header

It's **really recommended** to inform the server about what you expect for: json, csv, plain-text, xml, ...  To do this, use the `Accept` header like in the example here above. This is safer because the server can change his default format from JSON to CSV f.i. and if you expect JSON, your code will be broken.

Don't do this:

```javascript
const employee = axios.create({
    baseURL: 'http://localhost:3000/employees/123'
})
```

But well:

```javascript
const employee = axios.create({
    baseURL: 'http://localhost:3000/employees/123',
    headers: {
      'Accept': 'application/json'
    }
})
```

Now, in the second example, you are pretty sure `employee` contains json.
