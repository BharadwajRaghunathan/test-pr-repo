# PR Agent Test Repository

This repository serves as the **primary testbed** for validating the **PR Agent automated code review system**.  
It provides a controlled environment with sample Python files and pull requests to simulate real-world code changes, ensuring the **accuracy and reliability** of the automated review pipeline.

---

## 📌 Purpose

The repository is designed to:

- ✅ Test the PR Agent with controlled inputs.  
- ✅ Evaluate the quality and accuracy of static code analysis.  
- ✅ Demonstrate bug and style detection using intentionally flawed (`bad_code.py`) and clean (`good_code.py`) Python code.  
- ✅ Integrate with **GitHub Actions** or other CI/CD pipelines for **fully automated code review**.  
- ✅ Simulate pull requests that trigger the automated review workflow.  

---

## 📂 Repository Structure

```text
./
├── bad_code.py
├── good_code.py
├── .github/
│   └── workflows/
│       └── pr-review.yml
├── README.md

```
bad_code.py → Contains Python code with intentional issues (syntax errors, style violations, unused variables, unreachable code) to test detection capabilities.

good_code.py → Contains clean, well-structured Python code to validate that the review system correctly identifies minimal issues.

.github/workflows/pr-review.yml → Defines the GitHub Actions workflow that triggers the PR Agent automated review whenever Python files are modified in a pull request.

README.md → Documentation describing the repository’s purpose, structure, and usage.

🚀 Using This Repository

Create pull requests that involve changes to bad_code.py and/or good_code.py.

The PR Agent listens to pull request events via webhooks or CI workflows.

Automated reviews are triggered by the GitHub Actions workflow on every PR update.

Review results are posted back as comments on the pull request, including:

🐛 Detected bugs

🎨 Style and formatting issues

🔒 Security vulnerabilities

💡 Recommendations for improvements

The system also computes overall quality scores and flags potential risks.

⚙️ Integration with PR Agent

This repository acts as the input source for the PR Agent running on a backend server.

The PR Agent fetches changed files and analyzes them using:

Pylint

Flake8

AST parsing

Security scanning rules

Results are compiled into comprehensive reports and optionally posted as GitHub comments.

Supports both:

🔄 Fully automated workflows in CI/CD environments (e.g., GitHub Actions)

⚡ Manual API trigger calls

✅ Key Benefits

📊 Controlled test environment for reliable validation

🔁 Demonstrates end-to-end automation of code reviews

🧪 Ensures that both clean and problematic code cases are thoroughly tested

🚀 Enables continuous improvement of code quality through automation

