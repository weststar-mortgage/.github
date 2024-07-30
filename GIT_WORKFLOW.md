# Git Workflow

This document outlines the Git workflow we use at Weststar Mortgage.

## Overview

We use a simple branching model where each new feature or bug fix is developed in its own branch, based off the `main` branch. Changes are submitted through pull requests and reviewed before being merged.

## Branch Naming

- **Feature Branches**: `feat-brief-description`
- **Bug Fix Branches**: `fix-brief-description`

## Branching

1. **Update `main`**:
    ```sh
    git checkout main
    git pull origin main
    ```

2. **Create a Branch**:
    ```sh
    git checkout -b feat-brief-description
    ```

## Committing

1. **Stage Changes**:
    ```sh
    git add -A
    ```

2. **Commit Changes**: (see CONTRIBUTING.md for more details)
    ```sh
    git commit -m "Description of changes"
    ```

## Pushing

1. **Push Branch to GitHub**:
    ```sh
    git push origin feat-brief-description
    ```

## Pull Requests

1. **Create a Pull Request**: On GitHub, create a pull request from your branch to `main`.
2. **Description**: Provide a clear title and description for your pull request.
3. **Link Issues**: Reference any relevant issues.
    ```
    Resolves #13
    ```

## Code Review

1. **Review**: Team members will review your code and provide feedback.
2. **Update**: Make any requested changes and push them to your branch. They will be added to the existing pull request.
3. **Approval**: Once approved, the pull request can be merged.

## Merging

1. **Merge**: Use the "Create a merge commit" option to merge your changes into `main`.
2. **Delete Branch**: Delete the branch after it has been merged.

## Releasing

1. **Create Release**: In the "Releases" section of the repo, create a new release. 
2. **Tagging**: Choose a new tag name like v1.0.0, while adhering to [semantic versioning](https://semver.org/).
3. **Release Title**: Give title that is a brief summary of the changes.
4. **Release Notes**: Above the release notes, there is a "Generate Release Notes" button that can be automatically generated.
5. **Attach Artifacts**: Attach any build artifacts (perhaps the single publish file).
6. **Publish Release**: Click the "Publish Release" button to publish the release.

## Summary

- Always create a new branch for your work.
- Use clear and descriptive commit messages.
- Submit pull requests for review before merging.
- Follow the code style and guidelines.

Happy coding!
