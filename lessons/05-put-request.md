# Lesson 05 - PUT Request

## Objective

Understand how PUT requests are used to update existing resources.

## What is a PUT Request?

A PUT request is used to update an existing resource by replacing it entirely with the data provided in the request body.

If some fields are omitted, they may be overwritten depending on the API implementation.

## Syntax

```http
PUT /users/1
```

## Example API

```text
https://jsonplaceholder.typicode.com/users/1
```

## Request Body

```json
{
  "id": 1,
  "name": "Mohit Waghmare",
  "username": "mohit_updated",
  "email": "mohit.updated@example.com"
}
```

## Headers

```http
Content-Type: application/json
```

## Expected Response

The API returns the updated resource.

## Status Codes

### 200 OK

Resource updated successfully.

### 204 No Content

Resource updated successfully with no response body.

### 400 Bad Request

Invalid request data.

### 404 Not Found

Resource does not exist.

## PUT vs POST

POST:

* Creates a new resource

PUT:

* Updates an existing resource

## Common Use Cases

* Update user profile
* Update order information
* Update product details
* Modify account settings

## My Learning

* PUT is used to update existing resources.
* The request body contains the updated data.
* PUT generally replaces the entire resource.
* Successful updates commonly return 200 OK.
