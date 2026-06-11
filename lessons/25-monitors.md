# Lesson 25 - Monitors

## Objective

Understand Postman Monitors and how they help automatically verify API health and availability.

## What are Monitors?

Monitors are scheduled collection executions in Postman.

Instead of manually running requests, Postman executes them automatically at predefined intervals.

## Why Use Monitors?

Without Monitors:

* APIs are checked manually.
* Failures may go unnoticed.

With Monitors:

* APIs are checked automatically.
* Issues are detected earlier.
* Teams receive notifications.

## Typical Use Cases

### API Health Check

Verify critical APIs remain available.

### Production Monitoring

Monitor business-critical endpoints.

### Scheduled Regression Testing

Run automated tests regularly.

### SLA Validation

Track uptime and response times.

## Monitor Workflow

```text
Monitor Schedule
        ↓
Execute Collection
        ↓
Run Assertions
        ↓
Generate Results
        ↓
Notify Team
```

## Creating a Monitor

### Step 1

Select a collection.

### Step 2

Click:

```text
Monitor Collection
```

### Step 3

Configure:

* Collection
* Environment
* Frequency

### Step 4

Save Monitor.

## Example Schedule

```text
Every Hour
```

or

```text
Daily at 09:00 AM
```

## Example Assertion

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

If the assertion fails, the monitor reports failure.

## Benefits

* Automated validation
* Early issue detection
* Better reliability
* Reduced manual effort

## Limitations

Free plans may have execution limits.

Complex monitoring is often handled by dedicated monitoring platforms.

## QA Perspective

A QA Engineer should:

* Monitor critical APIs
* Validate response times
* Verify status codes
* Track recurring failures

## Common Interview Question

### What is the difference between Collection Runner and Monitor?

Collection Runner:

```text
Manual Execution
```

Monitor:

```text
Scheduled Automatic Execution
```

## My Learning

* Monitors execute collections automatically.
* They support scheduled API validation.
* They help detect issues early.
* They are useful for production monitoring.
