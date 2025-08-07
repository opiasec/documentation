---
title: Evaluators
---

# Evaluators

Evaluators are a crucial part of the Labs application, responsible for assessing user submissions and providing feedback. They can be used to evaluate various aspects of the lab, such as code quality, security vulnerabilities, and exploitability.

## SAST

Static Application Security Testing (SAST) evaluators analyze the user code for security vulnerabilities without executing it. They provide insights into potential security issues in the code, helping users to improve their coding practices and understand common vulnerabilities.

### About

SAST evaluator is based on Semgrep, a powerful static analysis tool that allows you to write custom rules to detect security vulnerabilities in code. More information about Semgrep can be found here: [Semgrep Documentation](https://semgrep.dev/docs/).

### Configuration

SAST evaluators have the following configuration options:
- **ERROR**: Value of penalty for errors found in the code. This needs to be a negative number, representing the penalty for each vulnerability with type `error` found.
    - Default Value: `-10`
- **WARNING**: Value of penalty for warnings found in the code. This needs to be a negative number, representing the penalty for each vulnerability with type `warning` found.
    - Default Value: `-5`
- **INFO**: Value of penalty for info messages found in the code. This needs to be a negative number, representing the penalty for each vulnerability with type `info` found.
    - Default Value: `-2`