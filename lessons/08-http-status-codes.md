# Lesson 08 - HTTP Status Codes

## Objective

Understand HTTP status codes and their significance in API testing.

## What are HTTP Status Codes?

HTTP status codes are returned by the server to indicate the outcome of a request.

They help clients understand whether a request was successful, failed, or requires further action.

## Status Code Categories

### 1xx - Informational

The request has been received and processing continues.

Examples:

* 100 Continue
* 101 Switching Protocols

### 2xx - Success

The request was processed successfully.

Examples:

* 200 OK
* 201 Created
* 202 Accepted
* 204 No Content

### 3xx - Redirection

Additional action is required to complete the request.

Examples:

* 301 Moved Permanently
* 302 Found
* 304 Not Modified

### 4xx - Client Errors

The request contains an error or cannot be fulfilled.

Examples:

* 400 Bad Request
* 401 Unauthorized
* 403 Forbidden
* 404 Not Found
* 405 Method Not Allowed
* 429 Too Many Requests

### 5xx - Server Errors

The server failed to process a valid request.

Examples:

* 500 Internal Server Error
* 502 Bad Gateway
* 503 Service Unavailable
* 504 Gateway Timeout

## Most Important Status Codes for API Testing

### 200 OK

Request completed successfully.

### 201 Created

Resource created successfully.

### 204 No Content

Request succeeded but no response body is returned.

### 400 Bad Request

Request data is invalid.

### 401 Unauthorized

Authentication is required.

### 403 Forbidden

Authentication succeeded but access is denied.

### 404 Not Found

Requested resource does not exist.

### 500 Internal Server Error

Unexpected server-side failure.

## What Should a Tester Validate?

* Correct status code is returned.
* Response body matches the status code.
* Error messages are meaningful.
* API behaves consistently.
* Invalid requests return appropriate errors.

## My Learning

* HTTP status codes indicate request outcomes.
* 2xx indicates success.
* 4xx indicates client-side issues.
* 5xx indicates server-side issues.
* Status code validation is a fundamental API testing activity.
