# Lesson 15 - Tests and Assertions

## Objective

Learn how to validate API responses automatically using Postman Tests and Assertions.

## What are Tests?

Tests are JavaScript snippets executed after a request receives a response.

They are used to validate whether the API behaves as expected.

Without tests:

* Requests are executed manually.
* Validation is performed by humans.

With tests:

* Validation is automated.
* Failures are identified immediately.

## What are Assertions?

Assertions are conditions that must be true.

If an assertion fails, the test fails.

Example:

```javascript
pm.response.to.have.status(200);
```

This assertion verifies that the API returns HTTP 200.

## Why are Tests Important?

Tests help verify:

* Status Codes
* Response Time
* Response Body
* Headers
* JSON Properties
* Business Rules

## Postman Test Structure

```javascript
pm.test("Test Name", function () {

});
```

Example:

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

## Common Assertions

### Status Code Validation

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

### Response Time Validation

```javascript
pm.test("Response time is less than 1000ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(1000);
});
```

### Response Body Contains Data

```javascript
pm.test("Response contains user data", function () {
    pm.response.to.have.body();
});
```

### Verify JSON Property Exists

```javascript
pm.test("User has an ID", function () {
    const jsonData = pm.response.json();
    pm.expect(jsonData.id).to.exist;
});
```

### Verify Header Exists

```javascript
pm.test("Content-Type header exists", function () {
    pm.response.to.have.header("Content-Type");
});
```

## Viewing Results

After execution:

* Green = Pass
* Red = Fail

Results appear in the Test Results tab.

## Best Practices

* Keep tests small and focused.
* Validate both success and failure scenarios.
* Use meaningful test names.
* Avoid hardcoded values where possible.

## My Learning

* Tests automate API validation.
* Assertions verify expected behavior.
* Postman uses JavaScript for test scripts.
* Automated validation improves test reliability.
