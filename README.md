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


7. Detached HEAD
```bash
git checkout remotes/origin/rokon_dev_2_feature_auth

```
Git fetches the remote: It pulls the reference for the remote branch origin/rokon_dev_2_feature_auth from the remote repository.
Detached HEAD: Since you are checking out a remote reference directly (instead of a local branch), Git enters a detached HEAD state. You are effectively "viewing" the code at that commit (5996a9f in your case), but not actively working on a branch.
You can make changes and commit in this state, but those commits won't be attached to any branch. If you switch to another branch, those commits could be lost unless you explicitly create a new branch to keep them.


Why Detached HEAD Happens
This state typically occurs when:

You want to inspect a specific commit or version of the code without affecting any active branch.
You want to make experimental changes without committing them to a branch immediately. This is often useful for testing something in isolation.
You want to make temporary changes, like bug fixes or quick adjustments, before deciding where to place them in your branch structure.



8. want to return to the previous branch you were on:
git switch -

9. Undoing the Detached HEAD State
If you don’t want to keep the changes and want to go back to your previous branch (or state), you can discard any changes made in the detached HEAD state:

bash
git switch <branch-name>  # Go back to a regular branch
git reset --hard    


10. Switch to the Remote Branch (rokon_dev_2_feature_auth) and Create a Local Tracking Branch
If you want to start working on the remote branch rokon_dev_2_feature_auth locally (so you can make commits), you should check it out and create a local branch that tracks the remote branch.

To switch to rokon_dev_2_feature_auth and create a local branch:

bash
Copy code
git checkout -b rokon_dev_2_feature_auth origin/rokon_dev_2_feature_auth
