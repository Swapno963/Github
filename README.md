# Github
Industry-level practices added here.


Steps for Effective Branch Usage
1. Create a New Branch for Each Task
Each branch should represent a single task, bug fix, or feature. This ensures clarity and organization in the repository.

Command to create a branch:

```bash
git checkout -b <branch-name>
```


2. Use Clear and Consistent Naming Conventions
Use a naming convention that indicates the purpose of the branch. Here are common patterns:

Features:
**feature/<feature-name>
Example: feature/user-authentication
**Bug Fixes:
bugfix/<bug-description>
Example: bugfix/fix-login-error
**Chores:
chore/<task-name>
Example: chore/update-dependencies
**Hotfixes:
hotfix/<urgent-fix>
Example: hotfix/critical-security-patch


3. Always Start from the Correct Base Branch
Ensure your new branch is based on the correct branch to avoid unnecessary conflicts:

For new features or bug fixes: Start from the main or develop branch.
For hotfixes: Start from the release branch (if applicable).
Command to create a branch from a specific branch:

```bash
git checkout -b <new-branch-name> <base-branch>
```


4. Commit Incrementally and Push Regularly
Make small, meaningful commits that correspond to the scope of the branch.
Push changes frequently to allow collaboration and avoid losing work:
```bash
git push origin <branch-name>
```


5. Keep Branches Updated
Regularly pull changes from the base branch to your feature branch to minimize merge conflicts:

```bash
git pull origin main
```

6. Delete Merged Branches
Once a branch has been successfully merged, delete it to keep the repository clean:

```bash
git branch -d <branch-name>
git push origin --delete <branch-name>
```
