# Branch Protection Rules

This file defines the branch protection rules for the repository.

## Main Branch Protection

- Require pull request reviews before merging
- Require status checks to pass before merging
- Require signed commits
- Include administrators in these restrictions
- Restrict who can push to matching branches

## Development Branch Guidelines

- Create feature branches for new development
- Use the naming convention: `feature/feature-name`
- Use the naming convention: `bugfix/bug-name` for bug fixes
- Use the naming convention: `docs/documentation-name` for documentation updates

## Merge Process

1. Create a feature branch from main
2. Develop and test changes
3. Create a pull request to merge back to main
4. Request review from at least one team member
5. Address any review comments
6. Merge only after approval
