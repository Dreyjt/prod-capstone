Project: GitOps Workflow with Trello + GitHub Actions

Project Overview

This project demonstrates a GitOps-style development workflow integrating task management, version control, and automation. The goal is to ensure code quality, visibility of work, and a smooth onboarding experience for new developers.
The system connects:
•	Trello for task tracking
•	GitHub for source control
•	GitHub Actions for CI/CD automation

All development is driven by tasks, and code changes are validated before merging into the main branch.
________________________________________

Architecture Explanation

The workflow follows a simple but effective architecture:

Trello (Task Management) → GitHub (Code & Branching) → GitHub Actions (Automation)

•	Each Trello card represents a unit of work
•	Each card maps to a feature branch
•	Each branch maps to a Pull Request
•	GitHub Actions enforces quality via linting and testing
•	Trello cards are automatically updated based on PR events
________________________________________

Workflow Description

1.	Create a Trello card (Backlog)
2.	Create a feature branch linked to the card
3.	Move card to In Progress
4.	Commit changes incrementally
5.	Push branch and create PR
6.	CI runs automatically (lint + tests)
7.	Card moves to Review/QA
8.	Merge PR after checks pass
9.	Card moves to Done
________________________________________

Commit Conventions

All commits follow this format:

[TRELLO-###] Short description

Examples:
•	[TRELLO-001] Add CI workflow
•	[TRELLO-002] Add edge case test

Rules:
•	Every commit must reference a Trello ID
•	Commits must be descriptive and incremental
________________________________________

Setup Instructions

1.	Clone the repository
2.	Install dependencies:
      pip install -r requirements.txt
3.	Run tests:
      pytest
4.	Run linting:
      flake8 .
________________________________________



Reflection Answers
1. Why use GitOps?
GitOps ensures that Git is the single source of truth for both infrastructure and application changes. It improves traceability, reproducibility, and collaboration by making all changes auditable through commits and pull requests.
2. Why enforce CI before merging?
CI ensures that all code meets quality standards before entering the main branch. It prevents broken code, enforces consistency, and reduces bugs in production.
3. Benefits of “1 card = 1 branch = 1 PR”?
This approach isolates work, improves traceability, and simplifies debugging. Each feature can be reviewed independently, reducing risk and improving team collaboration.
4. Why automate Trello updates?
Automation removes manual overhead, ensures consistency, and keeps task tracking aligned with actual development progress.
5. Challenges faced
The main challenge was integrating Trello API with GitHub Actions and handling dynamic card lookup. This was solved by extracting Trello IDs from PR titles and querying the API.

