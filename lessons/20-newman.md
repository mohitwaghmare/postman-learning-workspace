# Lesson 20 - Newman

## Objective

Learn how to execute Postman collections from the command line using Newman.

## What is Newman?

Newman is Postman's command-line collection runner.

It allows collections to run without opening the Postman application.

## Why Use Newman?

Benefits:

* Command-line execution
* Automation friendly
* CI/CD integration
* Test reporting
* Scheduled execution

## Architecture

```text
Postman Collection
        ↓
      Newman
        ↓
   Test Execution
        ↓
      Reports
```

## Installation

Verify Node.js:

```bash
node -v
npm -v
```

Install Newman globally:

```bash
npm install -g newman
```

Verify installation:

```bash
newman -v
```

## Running a Collection

Example:

```bash
newman run "Postman Learning.postman_collection.json"
```

## Running with Environment

Example:

```bash
newman run "Postman Learning.postman_collection.json" \
-e Development.postman_environment.json
```

## Execution Results

Newman displays:

* Requests
* Assertions
* Pass Count
* Fail Count
* Execution Time

Example:

```text
10 requests
15 assertions

✔ 15 passed
✖ 0 failed
```

## Why QA Engineers Use Newman

### Local Automation

Execute collections quickly.

### Regression Testing

Run complete suites repeatedly.

### CI/CD Pipelines

Execute tests automatically after code changes.

### Reporting

Generate execution reports.

## Common Commands

Run collection:

```bash
newman run collection.json
```

Run collection with environment:

```bash
newman run collection.json -e environment.json
```

Generate report:

```bash
newman run collection.json -r cli,html
```

## My Learning

* Newman is Postman's command-line runner.
* Collections can run without Postman UI.
* Newman is widely used in API automation.
* Newman is commonly integrated with CI/CD pipelines.
