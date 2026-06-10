# Lesson 16 - Collection Runner

## Objective

Learn how to execute multiple requests and automated tests together using Postman's Collection Runner.

## What is Collection Runner?

Collection Runner is a Postman feature that allows you to execute an entire collection or folder automatically.

Instead of running requests one by one, Collection Runner executes them in sequence.

## Why Use Collection Runner?

Without Collection Runner:

* Requests are executed manually.
* Tests are validated individually.
* Execution is time-consuming.

With Collection Runner:

* Multiple requests run automatically.
* Tests execute automatically.
* Results are consolidated.
* Regression testing becomes easier.

## Collection Runner Workflow

```text
Collection
    ↓
Execute Requests
    ↓
Run Tests
    ↓
Generate Results
```

## Benefits

* Faster execution
* Repeatable testing
* Reduced manual effort
* Better regression testing
* Easy result analysis

## Running a Collection

### Step 1

Select a Collection.

### Step 2

Click:

```text
Run Collection
```

### Step 3

Select:

* Collection
* Folder
* Environment

### Step 4

Execute the run.

### Step 5

Review results.

## Understanding Results

Collection Runner displays:

* Total Requests
* Passed Tests
* Failed Tests
* Execution Time

Example:

```text
Requests: 10
Passed: 18
Failed: 0
Duration: 2.1s
```

## Common Use Cases

### Smoke Testing

Verify critical APIs.

### Regression Testing

Validate existing functionality after changes.

### Environment Validation

Run tests against Dev, QA, and Production.

### Data-Driven Testing

Execute requests using external data files.

## Best Practices

* Keep collections organized.
* Add meaningful assertions.
* Use environments.
* Review failed tests carefully.
* Automate frequently executed scenarios.

## My Learning

* Collection Runner executes multiple requests automatically.
* Tests run automatically during execution.
* Collection Runner improves testing efficiency.
* It is a key feature for API automation.
