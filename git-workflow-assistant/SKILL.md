---
name: git-workflow-assistant
description: Guide developers through a standard Git workflow including syncing repositories, creating feature branches, reviewing changes, writing conventional commits, pushing to GitHub, and creating pull requests. Use whenever a user mentions starting an issue, creating a branch, committing code, pushing changes, opening a pull request, updating a repository, or needs help with Git workflow tasks.
---

# Git Workflow Assistant

## <ins>Purpose</ins>

Ensure developers follow a consistent and efficient Git workflow by syncing repositories, creating feature branches, reviewing changes, writing clear commit messages, pushing code to GitHub, and creating pull requests that are easy to review and understand.

## <ins>Procedure</ins>

1. Verify current branch and sync with main(or master):
- Check the current branch using `git branch`.
- If not on the main(or master) branch, switch to it using `git checkout main(or master)`.
- Pull the latest changes from the remote repository using `git pull origin main(or master)`.

2. Sync local repository with upstream:
- If the repository has an upstream remote, fetch the latest changes using `git fetch upstream`.
- Merge the upstream main(or master) branch into the local main(or master) branch using `git merge upstream/main(or master)`.

3. Create a feature branch:
- Create a new feature branch using `git checkout -b feature/your-feature-name`.

4. Review modified files before committing:
- Review modified files using `git status` to see which files have been changed.
- Inspect code changes using `git diff` before staging and committing to ensure code quality and correctness.

5. Generate clear commit messages using Conventional Commits:
- Follow the Conventional Commits format for commit messages, such as `feat: add new feature` or `fix: resolve bug in feature`.

6. Push changes to origin:
- Push the feature branch to the remote repository using `git push origin feature/your-feature-name`.

7. Create a pull request:
- Go to the GitHub repository and create a pull request from the feature branch to the main(or master) branch.
- Provide a clear title and description for the pull request, following the Conventional Commits format if applicable.
- Request reviews from team members and address any feedback received.
- Once approved, merge the pull request into the main(or master) branch and delete the feature branch if it is no longer needed.

8. Suggest verification steps before submission:
- Before pushing changes, suggest running tests or linters to ensure code quality.
- Encourage reviewing changes one last time before submitting the pull request.
- Remember to update any relevant documentation or changelogs as part of the commit messages or pull request description.

## <ins>Examples</ins>

### Example Input

"I need to start issue # 123, which involves adding a new feature to the project. I want to make sure I follow the correct Git workflow to keep everything organized and efficient."

### Example Output

1. Checkout the main(or master) branch and pull the latest changes:

```bash
git checkout main(or master)
git pull origin main(or master)
```

2. Pull upstream remote changes if applicable:

```bash
git fetch upstream
git merge upstream/main(or master)
```

3. Create a new feature branch:

```bash
git checkout -b feature/add-new-feature
```

4. After making changes, review modified files:

```bash
git status
git diff
```

5. Commit changes with a clear message:

```bash
git add .
git commit -m "feat: add new feature for issue # 123"
```

6. Push the feature branch to GitHub:

```bash
git push origin feature/add-new-feature
```

7. Open pull request on GitHub with a clear title and description, following the Conventional Commits format:

```bash
name: "feat: add new feature for issue # 123"
description: "This pull request adds a new feature to address issue # 123. It includes changes to the following files: ... Please review and provide feedback."
```

8. After receiving feedback, make necessary changes, commit them, and push to the same branch:

```bash
git add .
git commit -m "fix: address feedback for issue # 123"
git push origin feature/add-new-feature
```

9. Once the pull request is approved, merge it into the main(or master) branch and delete the feature branch if no longer needed:

```bash
git checkout main(or master)
git merge feature/add-new-feature
git push origin main(or master)
git branch -d feature/add-new-feature
```
