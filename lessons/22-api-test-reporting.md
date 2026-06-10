# Lesson 22 - API Test Reporting

## Objective

Learn how to generate API execution reports using Newman and understand why reporting is important in automation testing.

## Why Reporting Matters

Running tests is useful.

Understanding results is essential.

Reports help answer:

* Which tests passed?
* Which tests failed?
* When did failures occur?
* What was the response?
* How many assertions were executed?

## Types of Newman Reports

### CLI Report

Displayed directly in terminal.

Example:

```text
15 requests
3 assertions

✔ Passed
✖ Failed
```

### JSON Report

Machine-readable report.

Useful for integrations.

### HTML Report

Human-readable report.

Useful for:

* QA Teams
* Managers
* Stakeholders

## Installing HTML Reporter

Install globally:

```bash
npm install -g newman-reporter-html
```

Verify:

```bash
newman -v
```

## Generate HTML Report

Example:

```bash
newman run "collections/Postman Learning.postman_collection.json" ^
-e "environments/Development.postman_environment.json" ^
-r cli,html
```

## Custom Report Location

```bash
newman run "collections/Postman Learning.postman_collection.json" ^
-e "environments/Development.postman_environment.json" ^
-r cli,html ^
--reporter-html-export reports/newman-report.html
```

## Benefits

* Easy debugging
* Historical tracking
* Shareable results
* Better visibility

## Reporting in CI/CD

Typical flow:

```text
GitHub Actions
        ↓
Newman
        ↓
HTML Report
        ↓
Artifact
```

## My Learning

* Reports provide visibility into automation execution.
* Newman supports multiple report formats.
* HTML reports are useful for sharing results.
* Reporting is an important part of automation frameworks.
