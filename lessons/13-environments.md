# Lesson 13 - Environments

## Objective

Understand how Postman Environments help manage different deployment environments such as Development, QA, and Production.

## What is an Environment?

An Environment is a set of variables that can be switched easily within Postman.

Instead of manually changing URLs, tokens, and credentials, environments allow testers to switch contexts instantly.

## Why Use Environments?

Without Environments:

```text
https://dev-api.company.com
https://qa-api.company.com
https://prod-api.company.com
```

Every request must be edited manually.

With Environments:

```text
{{baseUrl}}
```

Only the variable value changes.

## Typical Environments

### Development

Used by developers for active development.

### QA

Used by testers for validation and testing.

### Production

Used by end users and customers.

## Example Environment Variables

### Development

| Variable | Value                       |
| -------- | --------------------------- |
| baseUrl  | https://dev-api.company.com |

### QA

| Variable | Value                      |
| -------- | -------------------------- |
| baseUrl  | https://qa-api.company.com |

### Production

| Variable | Value                   |
| -------- | ----------------------- |
| baseUrl  | https://api.company.com |

## Variable Resolution

Postman resolves variables using scope priority.

Common scopes:

* Local
* Data
* Environment
* Collection
* Global

Environment variables usually override collection variables with the same name.

## Benefits

* Faster environment switching
* Reduced manual effort
* Improved maintainability
* Better collaboration
* Reduced configuration mistakes

## Best Practices

* Store URLs in environments.
* Store tokens in environments.
* Avoid hardcoded values.
* Use meaningful environment names.

## My Learning

* Environments allow switching between systems easily.
* Environment variables improve maintainability.
* Real projects commonly use Dev, QA, and Production environments.
* Environment management is a key Postman skill.
