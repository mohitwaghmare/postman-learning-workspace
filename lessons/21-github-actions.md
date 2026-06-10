# Lesson 21 - GitHub Actions

## Objective

Learn how to automatically execute Postman collections using Newman whenever code is pushed to GitHub.

## What is GitHub Actions?

GitHub Actions is GitHub's built-in CI/CD platform.

It allows workflows to run automatically when events occur, such as:

* Pushes
* Pull Requests
* Scheduled Runs

## Why Use GitHub Actions?

Without GitHub Actions:

* Tests run manually.
* Failures may go unnoticed.

With GitHub Actions:

* Tests run automatically.
* Results are visible in GitHub.
* Issues are detected quickly.

## CI/CD Flow

```text
Developer Pushes Code
          ↓
GitHub Action Starts
          ↓
Install Newman
          ↓
Run Collection
          ↓
Display Results
```

## Workflow Location

GitHub Actions workflows are stored inside:

```text
.github/workflows
```

Example:

```text
.github/workflows/postman-tests.yml
```

## Workflow File

```yaml
name: Postman API Tests

on:
  push:
    branches:
      - main

jobs:
  run-postman-tests:

    runs-on: ubuntu-latest

    steps:

      - name: Checkout Repository
        uses: actions/checkout@v4

      - name: Install Newman
        run: npm install -g newman

      - name: Run Postman Collection
        run: |
          newman run "collections/Postman Learning.postman_collection.json" \
          -e "environments/Development.postman_environment.json"
```

## Workflow Explanation

### Checkout Repository

Downloads repository contents to the runner.

### Install Newman

Installs Newman on GitHub's virtual machine.

### Run Collection

Executes the exported collection using the exported environment.

## Benefits

* Continuous testing
* Early defect detection
* Automated validation
* Improved confidence

## Real Project Example

```text
Code Push
    ↓
GitHub Actions
    ↓
Newman
    ↓
API Tests
    ↓
Pass / Fail
```

## My Learning

* GitHub Actions enables automated API testing.
* Newman can run inside GitHub workflows.
* API tests can execute automatically after every push.
* CI/CD is a critical automation skill.
