**axios(config):** Requests can be made by passing the relevant config to axios.

#### [Request options](https://github.com/axios/axios#request-config)

**Name**|**Type**|**Details**
:-----:|:-----:|:-----:
url|string|server URL that will be used for the request
method|string|get | post | put | delete
headers|object|custom headers to be sent e.g. {'X-Requested-With':'XMLHttpRequest'}
data|object|data to be sent as the request body {firstName: 'Fred'}

#### [Response schema](https://github.com/axios/axios#response-schema)

The response for a request contains the following information.

**Name**|**Type**|**Details**
:-----:|:-----:|:-----:
data|object|response that was provided by the server {}
status|number|HTTP status code from the server response
statusText|string|HTTP status message from the server response
headers|object|"HTTP headers that the server responded with 


All header names are lower cased and can be accessed using the bracket notation.
Example:
```
'response.headers['content-type']'
```

#### [Request methods aliases](https://github.com/axios/axios#request-method-aliases)

-   axios.request(config)
-   axios.get(url[, config])
-   axios.delete(url[, config])
-   axios.head(url[, config])
-   axios.options(url[, config])
-   axios.post(url[, data[, config]])
-   axios.put(url[, data[, config]])
-   axios.patch(url[, data[, config]])

**NOTE:** When using the alias methods url, method, and data properties don't need to be specified in config.

## POST request example

```javascript
const response = await axios({
	method: "post",
	url: "https://jsonplaceholder.typecode.com/posts",
	headers: {
		'Content-type': 'application/json; charset=UTF-8'
		},
	data: {
		title: 'foo',
		body: 'bar',
		userId: 1,
	},
})
```

