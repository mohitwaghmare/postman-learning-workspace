# Lesson 18 - Swagger and OpenAPI

## Objective

Understand Swagger/OpenAPI and learn how API documentation can be used to generate Postman collections.

## What is OpenAPI?

OpenAPI Specification (OAS) is a standard format used to describe REST APIs.

It defines:

* Endpoints
* Methods
* Parameters
* Request Bodies
* Responses
* Authentication

The specification is machine-readable and can be imported into tools such as Postman.

## What is Swagger?

Swagger is a set of tools built around the OpenAPI Specification.

Common Swagger tools:

* Swagger Editor
* Swagger UI
* Swagger Codegen

Swagger UI provides interactive API documentation.

## Why Swagger is Important for QA?

Without Swagger:

* Tester manually discovers APIs.
* Documentation may be incomplete.
* Endpoints may be misunderstood.

With Swagger:

* API contract is clearly defined.
* Endpoints are documented.
* Request/Response structures are available.
* Collections can be generated automatically.

## Typical Swagger URL

```text
https://petstore.swagger.io/
```

## What Information Can Be Found?

### Endpoints

```http
GET /pet/{petId}
POST /pet
DELETE /pet/{petId}
```

### Parameters

```http
petId
```

### Request Bodies

```json
{
  "name": "Doggie",
  "status": "available"
}
```

### Responses

```json
{
  "id": 1,
  "name": "Doggie"
}
```

## Importing Swagger into Postman

Postman supports:

* OpenAPI 3.x
* Swagger 2.0

Import options:

* URL
* File
* Raw Content

Postman automatically generates requests and folders from the specification.

## Benefits

* Faster API onboarding
* Better documentation
* Reduced manual effort
* Easier test creation
* Improved collaboration

## QA Perspective

A tester should verify:

* Endpoints match documentation.
* Parameters are correctly implemented.
* Status codes match specifications.
* Request/Response schemas are accurate.

## My Learning

* OpenAPI is a standard API specification.
* Swagger provides tooling around OpenAPI.
* Postman can generate collections from Swagger specs.
* Swagger is commonly used by developers and testers.
