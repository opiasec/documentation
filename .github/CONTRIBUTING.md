# Contributing to OPIASEC

<!-- Update Repository Name -->
First off, thank you for considering contributing to OPIASEC's AppSec Labs! It's people like you that make this project such a great tool for the AppSec community. We're excited to see what you'll bring to our project.

This document outlines the process for contributing to our platform. Please read it carefully to ensure a smooth and effective collaboration.

## Code of Conduct

By participating in this project, you are expected to uphold our [Code of Conduct](CODE_OF_CONDUCT.md). Please read it before you start. All contributors are expected to follow it to help us keep this a welcoming and friendly environment.

## How Can I Contribute?

There are many ways to contribute, and all of them are valuable. You can:

* **Report Bugs:** If you find a bug, please open an issue using the "Bug Report" template. Provide as much detail as possible.
* **Suggest Enhancements:** Have an idea for a new feature or a new lab? We'd love to hear it. Open an issue using the "Feature Request" or "New Lab Proposal" template.
* **Improve Documentation:** If you find parts of our documentation confusing or incomplete, please submit a pull request with your improvements.
* **Write Code:** Help us fix bugs or implement new features.

If you're looking for a place to start, check out the issues tagged with `good first issue` or `help wanted`. You can find them here:

<!-- Adjust repository links -->
* Good First Issues: `https://github.com/opiasec/appseclabs-platform/labels/good%20first%20issue`
* Help Wanted: `https://github.com/opiasec/appseclabs-platform/labels/help%20wanted`

## Your First Code Contribution

Ready to contribute code? Here's the workflow our project follows.

### Step 1: Find or Create an Issue

<!-- Adjust issues tab link -->
Before you start writing code, please check our [Issues tab](https://github.com/opiasec/appseclabs-platform/issues) to see if there's an existing issue for what you want to do.

* If an issue exists, please leave a comment saying you'd like to work on it. This helps us avoid duplicated effort.
* If no issue exists, please create one first to discuss the proposed changes with the maintainers. For significant changes, please follow our RFC Process.

### Step 2: Fork the Repository

Click the "Fork" button at the top right of the repository page to create a personal copy of the project under your own GitHub account.

### Step 3: Set Up Your Development Environment

<!-- Adjust links -->
1.  **Clone your fork:**
    ```bash
    git clone [https://github.com/](https://github.com/)[YOUR_USERNAME]/appseclabs-platform.git
    cd appseclabs-platform
    ```

2.  **Add the `upstream` remote:** This will help you keep your fork in sync with the main project.
    ```bash
    git remote add upstream [https://github.com/](https://github.com/)opiasec/appseclabs-platform.git
    ```

3.  **Install dependencies:** Follow the instructions on README.md to install dependencies and test the software.

### Step 4: Create a New Branch

Create a descriptive branch name for your changes. This helps everyone understand what you're working on.

```bash
# Example for a new feature
git checkout -b feat/add-xss-lab

# Example for a bug fix
git checkout -b fix/resolve-login-issue
```

### Step 5: Write Your Code

Make your changes, write your code, and add your tests\! As you work, remember to:

  * Follow the existing code style.
  * Ensure your code is well-commented, especially in complex areas.
  * Add or update tests as appropriate.

### Step 6: Test Your Changes

Run our linter and automated tests to make sure your changes haven't broken anything.

<!-- Add linter instructions? -->

```bash
# Run ESLint to check for style issues
npm run lint
```

<!-- 
```bash
# Run all tests
npm run test
``` 
-->

### Step 7: Commit Your Changes

We use **Conventional Commits** to maintain a clear and readable git history. Please format your commit messages accordingly.

Your commit message should be structured as follows:

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

**Common types:**

  * `feat`: A new feature
  * `fix`: A bug fix
  * `docs`: Documentation only changes
  * `style`: Changes that do not affect the meaning of the code (white-space, formatting, etc)
  * `refactor`: A code change that neither fixes a bug nor adds a feature
  * `test`: Adding missing tests or correcting existing tests
  * `chore`: Changes to the build process or auxiliary tools

**Example:**

```
feat(labs): Add new stored XSS lab challenge
```

### Step 8: Push to Your Fork

Push your changes to your forked repository.

```bash
git push origin feat/add-xss-lab
```

### Step 9: Submit a Pull Request (PR)

1.  Go to the original repository on GitHub. You should see a prompt to create a Pull Request from your new branch.
2.  Make sure the PR is targeting the `main` branch of the upstream repository.
3.  Fill out the PR template with a clear title and description of your changes. Link the issue you are resolving (e.g., "Closes \#123").
4.  If your PR involves visual changes, please include screenshots or GIFs.

## The Review Process

Once you submit your PR, here's what to expect:

1.  **Automated Checks:** Our CI/CD pipeline (GitHub Actions) will automatically run the linter and tests. Make sure these checks pass.
2.  **Code Review:** One or more maintainers will review your code. We may ask for changes or improvements. This is a normal part of the process\! We are here to collaborate.
3.  **Approval and Merge:** Once your PR is approved and all checks are passing, a maintainer will merge your code into the `main` branch.

Congratulations, and thank you for your contribution\!

## Questions?

If you have any questions, feel free to reach out on our:
  * [Discord Server](https://discord.gg/xAkfKHRz)
  * [GitHub Discussions](https://github.com/orgs/AppSec-Digital/discussions)
