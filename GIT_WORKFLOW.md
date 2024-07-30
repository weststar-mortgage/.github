# Git Workflow

This document outlines the Git workflow we use in our project.

## Overview

We use a simple branching model where each new feature or bug fix is developed in its own branch, based off the `main` branch. Changes are submitted through pull requests and reviewed before being merged.

## Branch Naming

- **Feature Branches**: `feature/brief-description`
- **Bug Fix Branches**: `bugfix/brief-description`
- **Hotfix Branches**: `hotfix/brief-description`

## Branching

1. **Update `main`**:
    ```sh
    git checkout main
    git pull origin main
    ```

2. **Create a Branch**:
    ```sh
    git checkout -b feature/brief-description
    ```

## Committing

1. **Stage Changes**:
    ```sh
    git add .
    ```

2. **Commit Changes**:
    ```sh
    git commit -m "Description of changes"
    ```

## Pushing

1. **Push Branch to GitHub**:
    ```sh
    git push origin feature/brief-description
    ```

## Pull Requests

1. **Create a Pull Request**: On GitHub, create a pull request from your branch to `main`.
2. **Description**: Provide a clear title and description for your pull request.
3. **Link Issues**: Reference any relevant issues.

## Code Review

1. **Review**: Team members will review your code and provide feedback.
2. **Update**: Make any requested changes and push them to your branch. They will be added to the existing pull request.
3. **Approval**: Once approved, the pull request can be merged.

## Merging

1. **Squash and Merge**: Use the "Squash and merge" option to merge your changes into `main`.
2. **Delete Branch**: Delete the branch after it has been merged.

## Releasing

1. **Tagging**: Create a tag for the new release.
    ```sh
    git tag -a v1.0.0 -m "Release version 1.0.0"
    git push origin v1.0.0
    ```

2. **Release Notes**: Update the release notes on GitHub.

## Summary

- Always create a new branch for your work.
- Use clear and descriptive commit messages.
- Submit pull requests for review before merging.
- Follow the code style and guidelines.

Happy coding!
