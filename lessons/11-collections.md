# Lesson 11 - Postman Collections

## Objective

Understand Postman Collections and how they help organize, maintain, and execute API requests efficiently.

## What is a Collection?

A Collection is a group of related API requests stored together in Postman.

Collections help organize APIs by module, feature, project, or service.

## Why Use Collections?

Without Collections:

* Requests become difficult to manage.
* APIs are hard to find.
* Testing becomes repetitive.

With Collections:

* Better organization.
* Easier collaboration.
* Reusable requests.
* Automated execution.
* Easier documentation.

## Example Structure

```text
E-Commerce API
│
├── Authentication
│   ├── Login
│   └── Logout
│
├── Users
│   ├── Get Users
│   ├── Create User
│   └── Delete User
│
└── Orders
    ├── Create Order
    └── Get Order
```

## Collection Features

### Folders

Used to group related requests.

Example:

```text
Users API
Status Code Examples
Headers Examples
```

### Variables

Collections can store variables that can be reused across requests.

Example:

```text
{{baseUrl}}
```

### Authorization

Authentication can be configured once at the collection level.

### Tests

Tests can be added to requests and executed automatically.

### Documentation

Collections can act as API documentation.

## Best Practices

* Use meaningful request names.
* Group requests into folders.
* Use variables instead of hardcoded values.
* Keep collections modular.
* Add descriptions to requests.

## Real Project Example

```text
User Management API
│
├── Authentication
├── Users
├── Roles
├── Permissions
└── Audit Logs
```

## My Learning

* Collections help organize API requests.
* Folders improve maintainability.
* Collections support variables and authorization.
* Collections are the foundation for automation and API documentation.
