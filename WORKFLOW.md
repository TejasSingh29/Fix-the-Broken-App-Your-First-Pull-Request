# GitHub Team Workflow

## 1. Branching Strategy

Our team uses a feature-branch workflow to keep the `main` branch stable and releasable.

### Main Branch

* The `main` branch contains only reviewed and releasable code.
* Direct changes to `main` should be avoided.
* Changes are introduced through pull requests.

### Feature Branches

New work is created in a separate branch using the following naming convention:

```text
feature/[short-description]
```

Example:

```text
feature/data-ingestion
```

Bug fixes can use:

```text
fix/[short-description]
```

Documentation changes can use:

```text
docs/[short-description]
```

Branches are deleted after their pull requests are merged to keep the repository clean.

---

## 2. Commit Message Convention

The team follows a consistent commit message format:

```text
[type]: [description]
```

The following commit types are used:

* `feat` - Adds a new feature
* `fix` - Fixes a bug
* `docs` - Adds or updates documentation
* `refactor` - Changes code structure without changing functionality
* `chore` - Performs maintenance or configuration work

### Examples

```text
feat: add transaction data ingestion
```

```text
docs: document team github workflow
```

```text
fix: handle missing transaction values
```

Consistent commit messages make the project history easier to understand and enable automated changelog generation.

---

## 3. Pull Request Review Process

All significant changes are submitted through a Pull Request before being merged into `main`.

Our review process follows these rules:

1. A Pull Request must have at least one approval before merging.
2. The Pull Request should explain what changed and why.
3. Reviewers check:

   * Correctness
   * Code clarity
   * Data integrity
   * Test coverage
4. Commit messages are also reviewed to ensure they follow the team's convention.
5. Related GitHub issues should be linked to the Pull Request.
6. After the PR is approved and merged, the associated issue is closed.

---

## 4. GitHub Issue Tracking

Every new feature or bug fix starts with a GitHub issue.

Each issue should contain:

* A clear, action-oriented title
* A description explaining the objective and expected result
* At least one appropriate label
* An assigned team member

Issues provide context for development work and make responsibilities visible to the team.

An issue is closed when the corresponding Pull Request is successfully merged.

---

## 5. Typical Development Workflow

A team member follows these steps when starting new work:

```bash
git checkout main
git pull origin main
git checkout -b feature/[short-description]
```

After completing the work:

```bash
git add .
git commit -m "feat: describe the change"
git push origin feature/[short-description]
```

The developer then opens a Pull Request targeting `main`.

After review and approval, the Pull Request can be merged and the feature branch can be deleted.
