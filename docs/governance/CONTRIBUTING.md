# How to Contribute

First off, thank you for considering contributing to *opiasec*! It's people like you that make our projects great tools for the AppSec community. We're excited to see what you'll bring to our project.

This document outlines the process for contributing to our projects. Please read it carefully to ensure a smooth and effective collaboration.

:::info
We use a GitFlow workflow for managing contributions. This means that all contributions should be made through pull requests (PRs) against the `develop` branch of the repository. GitFlow Cheat Sheet: [GitFlow Cheat Sheet](https://danielkummer.github.io/git-flow-cheatsheet/).
:::
## Code of Conduct

By participating in this project, you are expected to uphold our [Code of Conduct](code-of-conduct.md). Please read it before you start. All contributors are expected to follow it to help us keep this a welcoming and friendly environment.

## How Can I Contribute?

There are many ways to contribute, and all of them are valuable. You can:

* **Report Bugs:** If you find a bug, please open an issue using the "Bug Report" template. Provide as much detail as possible.
* **Suggest Enhancements:** Have an idea for a new feature or a new lab? We'd love to hear it. Open an issue using the "Feature Request".
* **Improve Documentation:** If you find parts of our documentation confusing or incomplete, please [submit a pull request](https://github.com/opiasec/documentation/pulls) with your improvements.
* **Write Code:** Help us fix bugs or implement new features.


## Your First Code Contribution

Ready to contribute code? Here's the workflow our project follows.

### Step 1: Find or Create an Issue

Before you start writing code, please check our [Issues tab](https://github.com/opiasec/labs/issues) to see if there's an existing issue for what you want to do.

:::warning
* If an issue exists, please leave a comment saying you'd like to work on it. This helps us avoid duplicated effort.
* If no issue exists, please create one first to discuss the proposed changes with the maintainers.
:::
### Step 2: Fork the Repository

Click the "Fork" button at the top right of the repository page to create a personal copy of the project under your own GitHub account.

### Step 3: Set Up Your Development Environment

1.  **Clone your fork:**
    ```bash
    git clone [https://github.com/](https://github.com/)[YOUR_USERNAME]/[PROJECT_REPO].git
    cd [PROJECT_REPO]
    ```

2.  **Add the `upstream` remote:** This will help you keep your fork in sync with the main project.
    ```bash
    git remote add upstream [https://github.com/](https://github.com/)opiasec/[PROJECT_REPO].git
    ```

### Step 4: Create a New Branch

Create a descriptive branch name for your changes. This helps everyone understand what you're working on.

```bash
# Example for a new feature
git checkout -b feat/add-xss-lab

# Example for a bug fix
git checkout -b fix/resolve-login-issue
```

:::info
We use conventional branch naming conventions:
- `feature/` for new features
- `bugfix/` for bug fixes
- `hotfix/` for urgent fixes
- `release/` for branches preparing for a release
- `chore/` for non-code tasks (like documentation updates, dependency updates, etc.)

More information about conventional branch [Conventional Branch](https://conventional-branch.github.io/)
:::

### Step 5: Write Your Code

Make your changes, write your code, and add your tests\! As you work, remember to:

  * Follow the existing code style.
  * Ensure your code is well-commented, especially in complex areas.
  * Add or update tests as appropriate.

### Step 6: Test Your Changes

Run our linter and automated tests to make sure your changes haven't broken anything.


### Step 7: Commit Your Changes

We use **Conventional Commits** to maintain a clear and readable git history. Please format your commit messages accordingly.

Your commit message should be structured as follows:

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```
:::info
**Common types:**

  * `feat`: A new feature
  * `fix`: A bug fix
  * `docs`: Documentation only changes
  * `style`: Changes that do not affect the meaning of the code (white-space, formatting, etc)
  * `refactor`: A code change that neither fixes a bug nor adds a feature
  * `test`: Adding missing tests or correcting existing tests
  * `chore`: Changes to the build process or auxiliary tools

More information about conventional commits can be found here: [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/).

**Example:**

```
feat(labs): Add new stored XSS lab challenge
```
:::

### Step 8: Push to Your Fork

Push your changes to your forked repository.

```bash
git push origin feat/add-xss-lab
```

### Step 9: Submit a Pull Request (PR)

1.  Go to the original repository on GitHub. You should see a prompt to create a Pull Request from your new branch.
2.  Make sure the PR is targeting the `develop` branch of the upstream repository.
3.  Fill out the PR template with a clear title and description of your changes. Link the issue you are resolving (e.g., "Closes \#123").
4.  If your PR involves visual changes, please include screenshots or GIFs.

## The Review Process

Once you submit your PR, here's what to expect:

1.  **Automated Checks:** Our CI/CD pipeline (GitHub Actions) will automatically run the linter and tests. Make sure these checks pass.
2.  **Code Review:** One or more maintainers will review your code. We may ask for changes or improvements. This is a normal part of the process\! We are here to collaborate.
3.  **Approval and Merge:** Once your PR is approved and all checks are passing, a maintainer will merge your code into the `main` branch.

Congratulations, and thank you for your contribution\!

## Questions?

If you have any questions, feel free to reach out on our [Discord Server](https://discord.gg/hXdwCW7e87).