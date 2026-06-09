# Lesson 06 - DELETE Request

## Objective

Understand how DELETE requests are used to remove resources from a server.

## What is a DELETE Request?

A DELETE request is used to remove an existing resource identified by a specific endpoint.

The resource is usually identified using a path parameter.

## Syntax

```http
DELETE /users/1
```

## Example API

```text
https://jsonplaceholder.typicode.com/users/1
```

## Request Body

DELETE requests typically do not require a request body.

## Expected Response

The API may return:

* The deleted resource
* A confirmation message
* An empty response body

## Status Codes

### 200 OK

Resource deleted successfully.

### 202 Accepted

Deletion request accepted and will be processed.

### 204 No Content

Resource deleted successfully with no response body.

### 404 Not Found

Resource does not exist.

## Common Use Cases

* Delete a user account
* Delete a product
* Delete an order
* Remove a comment
* Remove uploaded files

## DELETE vs PUT

PUT:

* Updates an existing resource

DELETE:

* Removes an existing resource

## My Learning

* DELETE requests remove resources.
* The resource is usually identified using a path parameter.
* DELETE requests commonly return 200 OK or 204 No Content.
* Invalid resource identifiers may return 404 Not Found.
