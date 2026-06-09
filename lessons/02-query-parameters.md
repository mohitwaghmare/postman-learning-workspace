# Lesson 02 - Query Parameters

## Objective

Understand how query parameters are used to filter, sort, or modify data returned by an API.

## What are Query Parameters?

Query parameters are key-value pairs appended to a URL after a question mark (?).

They provide additional information to the server without changing the endpoint.

## Syntax

```text
https://api.example.com/users?key=value
```

Multiple query parameters can be added using the ampersand (&).

```text
https://api.example.com/users?page=1&limit=10
```

## Example API

https://jsonplaceholder.typicode.com/posts?userId=1

## Breakdown

Endpoint:

```text
/posts
```

Query Parameter:

```text
userId=1
```

Meaning:

Return only posts belonging to user ID 1.

## Common Use Cases

* Filtering data
* Searching records
* Pagination
* Sorting results
* Limiting response size

## Examples

Filter:

```text
/users?role=admin
```

Pagination:

```text
/users?page=2&limit=20
```

Search:

```text
/users?name=John
```

## Difference Between Query Parameters and Path Parameters

Query Parameters:

* Optional
* Used for filtering or searching
* Appear after ?

Path Parameters:

* Usually mandatory
* Identify a specific resource
* Part of the endpoint URL

Example:

```text
/users/1
```

Here, 1 is a path parameter.

## My Learning

* Query parameters help refine API responses.
* They are added after the ? symbol.
* Multiple parameters are separated using &.
* Query parameters are commonly used for filtering and pagination.
