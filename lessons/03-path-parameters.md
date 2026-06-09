# Lesson 03 - Path Parameters

## Objective

Understand how path parameters are used to identify and access specific resources in an API.

## What are Path Parameters?

Path parameters are dynamic values that form part of the API endpoint URL.

They are typically used to uniquely identify a resource.

## Syntax

```text
https://api.example.com/users/{id}
```

Example:

```text
https://jsonplaceholder.typicode.com/users/1
```

In this example, `1` is the path parameter.

## Example API

```text
https://jsonplaceholder.typicode.com/users/1
```

### Breakdown

Resource:

```text
users
```

Path Parameter:

```text
1
```

Meaning:

Return details for the user whose ID is 1.

## Path Parameters vs Query Parameters

### Path Parameters

* Used to identify a specific resource
* Usually required
* Part of the URL path

Example:

```text
/users/1
```

### Query Parameters

* Used to filter or modify results
* Usually optional
* Added after the `?` symbol

Example:

```text
/users?role=admin
```

## Common Use Cases

* Retrieve a user by ID
* Retrieve an order by order number
* Retrieve a product by product ID
* Retrieve employee details by employee ID

## Expected Response

The API returns a JSON object containing details of a single user.

## Status Code

200 OK

Meaning:

* Request was successful
* Resource was found and returned

## My Learning

* Path parameters uniquely identify resources.
* They are part of the endpoint URL.
* They are commonly used in REST APIs.
* Invalid resource identifiers often return 404 Not Found.
