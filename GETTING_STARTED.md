Getting Started Guide

This guide helps new contributors get up and running in under 1 hour.
________________________________________

Environment Setup

Requirements:
•	Python 3.10+
•	Git
Steps:
1.	Clone repository:
      git clone
2.	Navigate into project:
      cd your-repo-name
3.	Install dependencies:
      pip install -r requirements.txt
________________________________________

Running Tests
Run:
pytest
Expected:
All tests should pass
________________________________________

Running Linting
Run:
flake8 .
Fix any linting issues before committing.
________________________________________


Branch Workflow
1.	Switch to main:
      git checkout main
      git pull origin main
2.	Create new branch:
      git checkout -b feature/TRELLO-###-description
________________________________________

Creating a Pull Request
1.	Push branch:
git push origin feature/...
2.	Open PR on GitHub
3.	Title format:
[TRELLO-###] Description
4.	Wait for CI checks to pass
________________________________________

Troubleshooting

Tests failing
•	Check test output
•	Ensure dependencies installed
    Lint errors
•	Run flake8 and fix issues
    CI failing
•	Review GitHub Actions logs
•	Fix errors and push again
    Trello not updating
•	Verify API key and token
•	Check PR title includes Trello ID
________________________________________

Expected Setup Time
Under 1 hour for new contributors


