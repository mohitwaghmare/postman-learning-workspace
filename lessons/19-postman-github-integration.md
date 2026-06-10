# Lesson 19 - Postman and GitHub Integration

## Objective

Understand how Postman collections can be version-controlled using GitHub and how teams collaborate on API testing assets.

## Why Use GitHub with Postman?

As collections grow, changes need to be tracked and shared.

GitHub provides:

* Version control
* Collaboration
* Change history
* Backup
* CI/CD integration

## Approach 1 - Export and Commit

The most common approach.

Workflow:

```text
Postman
    ↓ Export Collection
JSON File
    ↓
GitHub Repository
```

Example:

```text
collections/
└── Postman Learning.postman_collection.json
```

### Advantages

* Simple
* Easy to understand
* Works everywhere
* Easy to review changes

### Disadvantages

* Manual export required
* Easy to forget updates

## Approach 2 - Git-Connected Collections

Postman can connect directly to Git repositories.

Workflow:

```text
Postman
    ↔
GitHub
```

### Advantages

* Automatic synchronization
* Better collaboration
* Enterprise-friendly

### Disadvantages

* More complex setup
* Less useful for learning repositories

## Why We Chose Export + GitHub

For this repository:

```text
Postman Learning Workspace
```

Exporting collections is preferred because:

* You learn collection structure.
* You can review JSON changes.
* Recruiters can inspect the artifacts.
* It mirrors how many teams still manage collections.

## What Should Be Stored in GitHub?

### Collections

```text
collections/
```

### Environments

```text
environments/
```

### Documentation

```text
lessons/
```

### Screenshots

```text
screenshots/
```

## What Should NOT Be Stored?

Never commit:

* Production secrets
* Real passwords
* Real API keys
* Real access tokens

## Recommended Repository Structure

```text
postman-learning-workspace/
│
├── lessons/
├── collections/
├── environments/
├── screenshots/
└── README.md
```

## Real Team Workflow

```text
Developer updates API
          ↓
Swagger updated
          ↓
QA updates collection
          ↓
Collection exported
          ↓
GitHub commit
          ↓
Newman execution
          ↓
CI/CD validation
```

## My Learning

* GitHub provides version control for Postman assets.
* Collections and environments should be stored in source control.
* Secrets should never be committed.
* GitHub enables automation using Newman and GitHub Actions.
