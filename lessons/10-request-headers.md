# Lesson 10 - Request Headers

## Objective

Understand the role of HTTP headers and how they are used in API requests and responses.

## What are Headers?

Headers are key-value pairs that provide additional information about an HTTP request or response.

They help the client and server communicate metadata about the request.

## Header Format

```http
Header-Name: Header-Value
```

Example:

```http
Content-Type: application/json
```

## Common Request Headers

### Content-Type

Specifies the format of the request body.

Example:

```http
Content-Type: application/json
```

### Accept

Specifies the response format expected by the client.

Example:

```http
Accept: application/json
```

### Authorization

Used to send authentication credentials.

Example:

```http
Authorization: Bearer eyJhbGciOi...
```

### User-Agent

Identifies the client application.

Example:

```http
User-Agent: PostmanRuntime/7.45.0
```

## Common Response Headers

### Content-Type

Indicates the format of the response.

Example:

```http
Content-Type: application/json
```

### Content-Length

Indicates the size of the response body.

Example:

```http
Content-Length: 509
```

### Date

Shows when the response was generated.

Example:

```http
Date: Mon, 09 Jun 2025 10:30:00 GMT
```

## Why Headers Matter in API Testing

A tester should verify:

* Required headers are present.
* Header values are correct.
* Content-Type matches the payload.
* Authentication headers work correctly.
* APIs reject invalid headers.

## Frequently Used Headers in Real Projects

```http
Content-Type
Accept
Authorization
Cache-Control
User-Agent
X-API-Key
```

## My Learning

* Headers provide metadata about requests and responses.
* Content-Type and Accept are among the most common headers.
* Authorization headers are used for secured APIs.
* Header validation is an important part of API testing.
