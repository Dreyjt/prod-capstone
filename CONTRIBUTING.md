Contributing Guide
________________________________________

Full Development Workflow
1.	Pick a Trello card
2.	Create feature branch
3.	Move card to In Progress
4.	Commit changes incrementally
5.	Push branch
6.	Open Pull Request
7.	CI runs automatically
8.	Merge after approval
9.	Card moves to Done
________________________________________

Branching Rules
•	main → stable code only
•	feature branches:
feature/TRELLO-###-description
Rules:
•	One branch per card
•	No direct commits to main
________________________________________

Commit Format

All commits must follow:
[TRELLO-###] Description
Examples:
•	[TRELLO-003] Add flake8 config
•	[TRELLO-002] Add new test case
________________________________________

Pull Request Process
1.	Create PR from feature branch → main
2.	Title must include Trello ID
3.	Ensure CI passes
4.	Review changes
5.	Merge PR
________________________________________

CI/CD Explanation

CI is implemented using GitHub Actions.
Pipeline includes:
•	Dependency installation
•	Linting with flake8
•	Testing with pytest
Automation:
•	PR opened → move card to Review/QA
•	PR merged → move card to Done
________________________________________

Coding Standards
•	Follow PEP8
•	Use meaningful variable names
•	Write readable and maintainable code
•	Add tests for new functionality
________________________________________

Failure Handling
If CI fails:
1.	Check logs in GitHub Actions
2.	Fix errors locally
3.	Re-run tests
4.	Push changes
If Trello automation fails:
•	Verify API credentials
•	Ensure correct list IDs
•	Check PR title format
________________________________________

Key Principles
•	Small, incremental commits
•	Clear traceability (card → branch → PR)
•	Automation for consistency
•	Maintain clean main branch


