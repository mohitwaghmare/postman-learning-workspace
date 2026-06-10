# Lesson 17 - Pre-request Scripts

## Objective

Understand how Pre-request Scripts work and how they help prepare data before an API request is executed.

## What are Pre-request Scripts?

Pre-request Scripts are JavaScript code snippets that execute before a request is sent.

They are commonly used to:

* Create variables
* Generate dynamic data
* Prepare authentication tokens
* Set timestamps
* Build request payloads

## Execution Flow

```text
Pre-request Script
        ↓
Request Sent
        ↓
Response Received
        ↓
Tests Executed
```

## Why Use Pre-request Scripts?

Without Pre-request Scripts:

* Values are hardcoded.
* Data becomes repetitive.
* Maintenance becomes difficult.

With Pre-request Scripts:

* Values can be generated dynamically.
* Requests become reusable.
* Automation becomes easier.

## Accessing Variables

Set a variable:

```javascript
pm.environment.set("userId", 1);
```

Get a variable:

```javascript
const userId = pm.environment.get("userId");
```

## Dynamic Timestamp

```javascript
pm.environment.set(
    "timestamp",
    new Date().toISOString()
);
```

## Dynamic Random Number

```javascript
const randomId = Math.floor(Math.random() * 1000);

pm.environment.set(
    "randomId",
    randomId
);
```

## Dynamic Random Email

```javascript
const email =
    "user" +
    Math.floor(Math.random() * 10000) +
    "@example.com";

pm.environment.set(
    "email",
    email
);
```

## Common Use Cases

### Generate Test Data

Avoid duplicate users.

### Create Tokens

Store authentication tokens.

### Generate Dates

Create dynamic timestamps.

### Build Payloads

Create reusable request bodies.

## Best Practices

* Keep scripts small.
* Use meaningful variable names.
* Avoid unnecessary logic.
* Store reusable values in variables.

## My Learning

* Pre-request Scripts run before a request is sent.
* They use JavaScript.
* They help create dynamic data.
* They improve automation and reusability.
