# GitHub Team Workflow

## 1. Branching Strategy

Our team uses a feature-branch workflow to keep the `main` branch stable and releasable.

### Main Branch
- The `main` branch contains only reviewed and releasable code.
- Direct changes to `main` should be avoided.
- Changes are introduced through Pull Requests.

### Feature Branches
New work is created in a separate branch using:

`feature/[short-description]`

Example:

`feature/data-ingestion`

Branches are deleted after their Pull Requests are merged.

---

## 2. Commit Message Convention

The team follows this format:

`[type]: [description]`

Types used:

- `feat` - New feature
- `fix` - Bug fix
- `docs` - Documentation
- `refactor` - Code restructuring
- `chore` - Maintenance work

Examples:

`feat: add transaction data ingestion`

`docs: document team github workflow`

`fix: handle missing transaction values`

Consistent commit messages make the project history easier to understand and enable automated changelog generation.

---

## 3. Pull Request Review Process

All significant changes are submitted through a Pull Request before being merged into `main`.

- PRs require at least one approval before merge.
- Code review focuses on correctness, clarity, data integrity, and test coverage.
- Commit messages are reviewed as part of code review.
- Related GitHub issues should be linked to Pull Requests.
- Issues are closed when the corresponding PR is merged.

---

## 4. GitHub Issue Tracking

Every feature or fix starts with a GitHub issue.

Each issue should contain:

- A clear action-oriented title
- A description explaining the objective and expected result
- At least one appropriate label
- An assigned team member

Issues provide context for development work and make responsibilities visible to the team.

Issues are closed when the corresponding Pull Request is merged.

---

## 5. Development Workflow

A team member starts new work by updating `main` and creating a feature branch:

```bash
git checkout main
git pull origin main
git checkout -b feature/[short-description]