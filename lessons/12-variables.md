# Lesson 12 - Variables

## Objective

Understand how variables help create reusable and maintainable Postman requests.

## What are Variables?

Variables are placeholders used to store values that can be reused across requests.

Instead of hardcoding values, variables make collections flexible and easier to maintain.

## Variable Syntax

```text
{{variableName}}
```

Example:

```text
{{baseUrl}}/users
```

## Why Use Variables?

Without Variables:

```text
https://jsonplaceholder.typicode.com/users
https://jsonplaceholder.typicode.com/posts
https://jsonplaceholder.typicode.com/comments
```

If the domain changes, every request must be updated.

With Variables:

```text
{{baseUrl}}/users
{{baseUrl}}/posts
{{baseUrl}}/comments
```

Only one value needs to be changed.

## Types of Variables

### Global Variables

Available across all collections.

Example:

```text
baseUrl
```

### Collection Variables

Available only within a specific collection.

Example:

```text
userId
```

### Environment Variables

Available within a selected environment.

Example:

```text
devUrl
qaUrl
prodUrl
```

### Local Variables

Used only during request execution.

## Creating a Collection Variable

Name:

```text
baseUrl
```

Value:

```text
https://jsonplaceholder.typicode.com
```

## Using Variables

Instead of:

```text
https://jsonplaceholder.typicode.com/users
```

Use:

```text
{{baseUrl}}/users
```

## Benefits

* Reusability
* Easier maintenance
* Faster environment switching
* Reduced duplication
* Better collaboration

## Best Practices

* Use collection variables whenever possible.
* Avoid hardcoded URLs.
* Use meaningful variable names.
* Store environment-specific values in environments.

## My Learning

* Variables reduce hardcoding.
* Variables make collections reusable.
* Collection variables are ideal for shared values.
* Environment variables help support multiple environments.
