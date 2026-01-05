---
title: Internet Access
type: docs
weight: 1
# prev: /
# next: docs/folder/
---

## Declaration

```yaml
imports:
  my_http_client:
    http_client:
      # Declare the website you want to access
      baseUrl: https://example.com
      
      # Optionally add headers
      headers:
        HEADER1: VALUE
```

## JavaScript API

### Methods

- `get(path) -> JsHttpResponse`: make a GET request to `{baseUrl}/{path}`
- `delete(path) -> JsHttpResponse`: make a DELETE request to `{baseUrl}/{path}`
- `head(path) -> JsHttpResponse`: make a HEAD request to `{baseUrl}/{path}`
- `options(path) -> JsHttpResponse`: make a OPTIONS request to `{baseUrl}/{path}`
- `post(path, body)`: make a POST request to `{baseUrl}/{path}`
  - `body` (HttpBody): Request body. Can be either a string or JSON object
- `put(path, body)`: make a PUT request to `{baseUrl}/{path}`
  - `body` (HttpBody): Request body. Can be either a string or JSON object
- `patch(path, body)`: make a PATCH request to `{baseUrl}/{path}`
  - `body` (HttpBody): Request body. Can be either a string or JSON object
- `setOauth(credentials)`: see [oauth](../oauth) for usage.
- `withOptions(opts)`: returns a new client object with the selected options. Good for setting HTTP headers.
  - `opts` (HttpOptions): options object

### Objects

- `JsHttpResponse`
  - `statusCode` (int): Status code for the HTTP response
  - `headers` (object): Headers returned by the HTTP response
  - `body` (HttpBody): Response Body
- `HttpBody`
  - `string` (string): The HTTP response body as a string
  - `json` (object): The HTTP body marshalled to JSON. This will be null if the response is not valid JSON.
- `HttpOptions`
  - `headers` (object): HTTP headers to add to the client
  - `mergeHeaders` (bool): Set to false to ignore the headers on the parent client.

## Example

```javascript
var response = my_http_client.get("/some/api");
console.log(response.statusCode);
console.log(response.body.json);
console.log(response.body.string);

var withCreds = my_http_client.withOptions({headers: {"Authorization": "Token 1234"}});
withCreds.post("/some/api", {json:{hello: "world"}});
```
