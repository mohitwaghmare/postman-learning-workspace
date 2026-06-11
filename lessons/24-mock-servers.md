# Lesson 24 - Mock Servers

## Objective

Understand Mock Servers and how they help API development and testing when backend services are unavailable.

## What is a Mock Server?

A Mock Server simulates the behavior of a real API.

It returns predefined responses without requiring an actual backend implementation.

## Why Mock Servers Are Needed

In real projects:

```text
Frontend Team Ready
QA Team Ready
Backend Team Not Ready
```

Without Mock Servers:

* Development is blocked.
* Testing is delayed.

With Mock Servers:

* Development continues.
* Testing starts early.
* Teams work independently.

## Example

Real API:

```http
GET /users/1
```

Response:

```json
{
  "id": 1,
  "name": "Mohit"
}
```

Mock Server:

Returns the same response without calling a real database.

## Benefits

### Parallel Development

Teams can work simultaneously.

### Early Testing

QA can begin before backend completion.

### Predictable Responses

Responses remain consistent.

### Reduced Dependencies

Testing is not blocked by unavailable services.

## Mock Servers in Postman

Postman supports built-in Mock Servers.

Workflow:

```text
Collection
    ↓
Examples
    ↓
Mock Server
    ↓
Mock Endpoint
```

## Creating a Mock Server

### Step 1

Create a request:

```http
GET /users/1
```

### Step 2

Add an example response:

```json
{
  "id": 1,
  "name": "Mock User"
}
```

### Step 3

Create Mock Server.

### Step 4

Postman generates a mock URL.

Example:

```text
https://abc123.mock.pstmn.io/users/1
```

## QA Use Cases

* Contract Testing
* Frontend Testing
* Service Virtualization
* Failure Simulation

## Common Interview Question

### Why use Mock Servers?

Answer:

Mock Servers allow testing and development to continue even when dependent systems are unavailable.

## My Learning

* Mock Servers simulate real APIs.
* They reduce dependency on backend systems.
* They enable earlier testing.
* Postman provides built-in Mock Server support.
