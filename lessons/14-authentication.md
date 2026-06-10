# Lesson 14 - Authentication

## Objective

Understand how APIs authenticate users and applications before granting access to resources.

## What is Authentication?

Authentication is the process of verifying the identity of a user or application.

Most production APIs require authentication to protect sensitive data and functionality.

## Why Authentication is Important

Without authentication:

* Anyone can access APIs.
* Sensitive data can be exposed.
* Unauthorized actions can be performed.

Authentication ensures only authorized users and systems can access protected resources.

## Common Authentication Methods

### 1. API Key Authentication

The client sends a unique key with each request.

Example:

```http
X-API-Key: abc123xyz
```

Advantages:

* Simple to implement
* Easy to use

Limitations:

* Less secure if exposed

---

### 2. Basic Authentication

Credentials are sent as:

```http
Authorization: Basic base64(username:password)
```

Example:

```http
Authorization: Basic bW9oaXQ6cGFzc3dvcmQ=
```

Advantages:

* Simple

Limitations:

* Requires HTTPS
* Credentials are reusable

---

### 3. Bearer Token Authentication

The client sends an access token.

Example:

```http
Authorization: Bearer eyJhbGciOiJIUzI1Ni...
```

Advantages:

* Widely used
* More secure than Basic Auth

---

### 4. JWT (JSON Web Token)

A JWT contains encoded information about the user.

Structure:

```text
Header.Payload.Signature
```

Example:

```text
eyJhbGciOiJIUzI1Ni...
```

JWTs are commonly used in modern web applications and REST APIs.

---

### 5. OAuth 2.0 (Overview)

OAuth allows third-party applications to access resources without exposing user credentials.

Examples:

* Sign in with Google
* Sign in with GitHub
* Sign in with Microsoft

OAuth is widely used in enterprise systems.

## Authentication vs Authorization

### Authentication

Who are you?

Example:

```text
Login
```

### Authorization

What are you allowed to do?

Example:

```text
Admin can delete users.
Viewer can only read users.
```

## Authentication in Postman

Postman supports:

* No Auth
* API Key
* Basic Auth
* Bearer Token
* OAuth 2.0

Authentication can be configured:

* Request Level
* Folder Level
* Collection Level

## Best Practices

* Never hardcode secrets.
* Store tokens in environments.
* Use HTTPS.
* Rotate credentials regularly.
* Use least-privilege access.

## My Learning

* Authentication verifies identity.
* APIs commonly use API Keys and Bearer Tokens.
* JWT is a common token format.
* Authentication and Authorization are different concepts.
* Postman provides built-in authentication support.
