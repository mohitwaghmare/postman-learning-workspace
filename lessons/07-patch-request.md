# Lesson 07 - PATCH Request

## Objective

Understand how PATCH requests are used to partially update existing resources.

## What is a PATCH Request?

A PATCH request is used to modify specific fields of an existing resource without replacing the entire resource.

Unlike PUT, only the fields that need to be changed are sent in the request body.

## Syntax

```http
PATCH /users/1
```

## Example API

```text
https://jsonplaceholder.typicode.com/users/1
```

## Request Body

```json
{
  "email": "mohit.updated@example.com"
}
```

## Headers

```http
Content-Type: application/json
```

## Expected Response

The API returns the updated resource containing the modified field(s).

## Status Codes

### 200 OK

Resource updated successfully.

### 204 No Content

Update completed successfully without a response body.

### 400 Bad Request

Invalid request data.

### 404 Not Found

Resource does not exist.

## PUT vs PATCH

### PUT

* Replaces the entire resource
* Sends all fields

Example:

```json
{
  "id": 1,
  "name": "Mohit",
  "username": "mohitw",
  "email": "mohit@example.com"
}
```

### PATCH

* Updates only specific fields
* Sends only the fields that need modification

Example:

```json
{
  "email": "mohit.updated@example.com"
}
```

## Common Use Cases

* Update email address
* Change account status
* Update profile picture
* Modify user preferences

## My Learning

* PATCH is used for partial updates.
* Only modified fields are sent in the request body.
* PATCH is generally more efficient than PUT.
* Understanding PUT vs PATCH is a common API testing interview topic.
