# github-actions-ci-pipeline
Automated CI pipeline using GitHub Actions
# GitHub Actions CI/CD Pipeline

## Project Overview

This project demonstrates the implementation of an automated Continuous Integration (CI) pipeline using GitHub Actions.

The pipeline automatically checks out source code, configures a Python environment, installs dependencies, builds the application, and runs automated tests.

## Technologies Used

- GitHub Actions — CI automation
- Python 3.11 — Application runtime
- pytest — Automated testing
- YAML — Workflow configuration
- Ubuntu — GitHub-hosted runner

## Repository Structure

```text
github-actions-ci-pipeline/
├── .github/
│   └── workflows/
│       └── ci.yml
├── app.py
├── test_app.py
├── requirements.txt
└── README.md
```

## CI Pipeline Configuration

The workflow is defined in `.github/workflows/ci.yml`.

### Workflow Steps

1. **Event Triggers:** Automatically starts the pipeline when code is pushed to the main branch or a pull request targets main.
2. **Runner Environment:** Uses an Ubuntu GitHub-hosted runner.
3. **Repository Checkout:** Downloads the repository source code using `actions/checkout`.
4. **Python Setup:** Configures Python 3.11 using `actions/setup-python`.
5. **Dependency Installation:** Installs Python dependencies from `requirements.txt`.
6. **Application Build:** Validates and executes the Python application.
7. **Automated Testing:** Runs the pytest test suite to verify application functionality.
8. **Security and Optimization:** Uses pip dependency caching and supports encrypted GitHub Actions repository secrets.

## Automated Test Results

The pipeline successfully executed three automated tests:

| Test | Result |
|---|---|
| test_add | PASSED |
| test_subtract | PASSED |
| test_multiply | PASSED |

**Final result: 3 passed in 0.01 seconds.**

## Workflow Execution

The GitHub Actions workflow completed successfully, including repository checkout, Python setup, dependency installation, application build, and automated testing.

## Troubleshooting

During workflow execution, GitHub displayed a warning that Node.js 20 was deprecated for the versions of `actions/checkout` and `actions/setup-python` used.

GitHub automatically ran these actions using Node.js 24, allowing the pipeline to complete successfully.

An additional informational notice concerned the migration of the `ubuntu-latest` runner image.

Neither annotation caused the pipeline to fail.

## Conclusion

This project demonstrates how GitHub Actions can automate application builds and testing. The completed CI pipeline provides automatic validation of code changes, improves development reliability, and introduces security and dependency-caching practices.
