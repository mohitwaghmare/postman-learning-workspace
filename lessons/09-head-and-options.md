# Lesson 09 - HEAD and OPTIONS Requests

## Objective

Understand the purpose of HEAD and OPTIONS HTTP methods and when they are used in API testing.

## HEAD Request

### What is a HEAD Request?

A HEAD request is similar to a GET request, but the server returns only the response headers and not the response body.

### Syntax

```http
HEAD /users/1
```

### Example API

```text
https://jsonplaceholder.typicode.com/users/1
```

### Response

A HEAD request returns:

* Status Code
* Response Headers

It does not return:

* Response Body

### Common Use Cases

* Verify resource availability
* Check Content-Type
* Check Content-Length
* Check Last-Modified date
* Performance optimization

### Example Headers

```http
Content-Type: application/json
Content-Length: 509
```

## OPTIONS Request

### What is an OPTIONS Request?

An OPTIONS request is used to discover which HTTP methods are supported by an endpoint.

### Syntax

```http
OPTIONS /users
```

### Example API

```text
https://jsonplaceholder.typicode.com/users
```

### Typical Response

```http
Allow: GET, POST, PUT, PATCH, DELETE
```

### Common Use Cases

* API exploration
* Discover supported methods
* CORS preflight requests
* Security testing

## HEAD vs GET

### GET

Returns:

* Headers
* Response Body

### HEAD

Returns:

* Headers only

No response body is returned.

## OPTIONS vs GET

### GET

Retrieves resource data.

### OPTIONS

Retrieves information about supported operations.

## Importance for API Testing

A tester can use HEAD requests to:

* Validate resource existence
* Verify metadata
* Reduce network usage

A tester can use OPTIONS requests to:

* Verify supported methods
* Validate API contracts
* Investigate endpoint capabilities

## My Learning

* HEAD returns headers without a response body.
* OPTIONS returns information about supported HTTP methods.
* Both methods are useful during API exploration and testing.
* Understanding HEAD and OPTIONS helps build a complete understanding of HTTP.
