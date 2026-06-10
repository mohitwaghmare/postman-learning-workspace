# Lesson 23 - API Versioning

## Objective

Understand API versioning, why it is important, and how QA engineers test versioned APIs.

## What is API Versioning?

API Versioning is the practice of managing changes to APIs without breaking existing clients.

As APIs evolve, new functionality may be added or existing behavior may change.

Versioning helps maintain compatibility.

## Why API Versioning is Needed

Imagine Version 1 returns:

```json
{
  "id": 1,
  "name": "Mohit"
}
```

Later, developers change it to:

```json
{
  "userId": 1,
  "fullName": "Mohit Waghmare"
}
```

Existing applications would break.

Versioning prevents this issue.

## Common Versioning Approaches

### URI Versioning

Most common.

Example:

```http
GET /api/v1/users
GET /api/v2/users
```

### Header Versioning

Example:

```http
API-Version: 2
```

### Query Parameter Versioning

Example:

```http
GET /users?version=2
```

## Version Lifecycle

```text
v1
 ↓
v2 Released
 ↓
v1 Deprecated
 ↓
v1 Removed
```

## Backward Compatibility

Backward compatibility means older clients continue working after new versions are released.

Example:

```text
Mobile App v1
        ↓
API v2 Released
        ↓
App Continues Working
```

## Deprecation

Before removing an API version, teams usually mark it as deprecated.

Example:

```http
Warning: API v1 is deprecated and will be removed on 31-Dec-2026
```

## QA Testing Considerations

A QA Engineer should verify:

* v1 continues to work
* v2 behaves as expected
* Response schemas are correct
* Backward compatibility is maintained
* Deprecation notices are documented

## Common Interview Question

### What would you test when API v2 is released?

Answer:

* Existing v1 functionality
* New v2 functionality
* Backward compatibility
* Schema changes
* Authentication behavior
* Error handling

## Real World Examples

```text
/api/v1/users
/api/v2/users
/api/v3/users
```

Many enterprise systems support multiple versions simultaneously.

## My Learning

* API versioning prevents breaking existing consumers.
* URI versioning is the most common strategy.
* QA engineers must validate both old and new versions.
* Backward compatibility is a critical testing concern.
