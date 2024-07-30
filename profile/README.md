# Weststar Mortgage Documentation

Welcome to the Weststar Mortgage GitHub organization! This documentation is designed to help you get started with Git, GitHub, and our workflow.

## Getting Started

1. **Install Git**: If you haven't already, download and install Git from [git-scm.com](https://git-scm.com/).
2. **Set Up Git**: Configure your Git username and email.
   ```sh
   git config --global user.name "Your Name"
   git config --global user.email "your.email@example.com"
   ```
3. **Clone the Repository**: Clone the repository to your local machine.
   ```sh
   git clone https://github.com/weststar-mortgage/RepositoryName.git
   cd RepositoryName
   ```

## Branching and Pull Requests

We follow a branching model where each feature or fix is developed in its own branch off of the `main` branch. Follow these steps to create a branch, make changes, and submit a pull request:

### Creating a Branch

1. **Fetch the latest changes from `main`**:

   ```sh
   git checkout main
   git pull origin main
   ```

2. **Create a new branch**:
   ```sh
   git checkout -b your-branch-name
   ```

### Making Changes

1. **Make your changes**: Edit files, add new files, and so on.
2. **Stage your changes**: Add the files you changed to the staging area.

   ```sh
   git add -A
   ```

3. **Commit your changes**: Commit your changes with a meaningful message. (see CONTRIBUTING.md for more details)
   ```sh
   git commit -m "Brief description of your changes"
   ```

### Pushing Changes and Creating a Pull Request

1. **Push your branch to GitHub**:

   ```sh
   git push origin your-branch-name
   ```

2. **Create a Pull Request**:
   - Go to the repository on GitHub.
   - Click the "Compare & pull request" button next to your branch.
   - Provide a title and description for your pull request.
   - Click "Create pull request".

### Reviewing Pull Requests

1. **Review Process**: Team members will review your code. They might suggest changes or approve your pull request.
2. **Make Changes**: If changes are requested, make them in your branch, commit, and push them. They will automatically be added to the existing pull request.
3. **Merge**: Once your pull request is approved, it can be merged into the `main` branch.

## Additional Resources

- [GitHub Docs](https://docs.github.com/en)
- [Git Documentation](https://git-scm.com/doc)
- [GitHub Learning Lab](https://lab.github.com/)
