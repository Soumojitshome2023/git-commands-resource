Git Commands
============

_A list of my commonly used Git commands_

---

### **Add Changes to a GitHub Repository :**

| Command                                                | Description                                                                        |
| ------------------------------------------------------ | ---------------------------------------------------------------------------------- |
| `git add .`                                            | Stage changes: If you have new changes to push, first add them to the staging area |
| `git commit -m "Your descriptive commit message here"` | Commit changes: Commit your changes with a message                                 |
| `git push origin main`                                 | Push changes: Now, push your local main branch to the remote repository            |

---

### **Add a Remote GitHub Repository :**

| Command                                                                 | Description                                                                                                               |
| ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| `git init`                                                              | Initialize a Git Repository (if you haven't already)<br />If your project is not already a Git repository, initialize one |
| `git remote add origin https://github.com/USERNAME/REPOSITORY_NAME.git` | Add a Remote GitHub Repository<br />Use the following command to add your GitHub repository as a remote                   |
| `git remote -v`                                                         | Verify the Remote<br />You can check if the remote repository was added successfully                                      |

---

### **Reset Changes to a GitHub Repository :**

```
git reset --hard <commit hash>
```

```
git push -f origin <branch>
```

---

### Getting & Creating Projects

| Command                                                           | Description                                |
| ----------------------------------------------------------------- | ------------------------------------------ |
| `git init`                                                        | Initialize a local Git repository          |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

---

### Sync your branch with the master branch using a specific commit hash from the master

| Command                                        | Description                                                                       |
| ---------------------------------------------- | --------------------------------------------------------------------------------- |
| `git fetch origin master`                      | Fetch the latest changes from the master branch                                   |
| `git checkout <your-branch>`                   | Switch to the branch that you want to sync with the master                        |
| `git rebase <commit-hash>`                     | You can now rebase your branch to the specific commit hash from the master branch |
| `git rebase --continue`                        | Resolve conflicts (if any)                                                        |
| `git push --force-with-lease`                  | Force push (if necessary)                                                         |
| `git push --set-upstream origin <your-branch>` | To push the current branch and set the remote as upstream                         |

---

### To merge the commits from the your-branch branch into the master branch

| Command                   | Description                                                                                                    |
| ------------------------- | -------------------------------------------------------------------------------------------------------------- |
| `git checkout master`     | Switch to the master branch                                                                                    |
| `git pull origin master`  | Pull the latest changes from the remote repository                                                             |
| `git merge <your-branch>` | Merge the xyz branch into master                                                                               |
| `git add .`               | If there are any merge conflicts, resolve them manually.<br />After resolving the conflicts, stage the changes |
| `git commit -m "message"` | Complete the merge by committing                                                                               |
| `git push origin master`  | Push the updated master branch to the remote repository                                                        |


---

### Basic Snapshotting

| Command                            | Description                                            |
| ---------------------------------- | ------------------------------------------------------ |
| `git status`                       | Check status                                           |
| `git add [file-name.txt]`          | Add a file to the staging area                         |
| `git add -A`                       | Add all new and changed files to the staging area      |
| `git commit -m "[commit message]"` | Commit changes                                         |
| `git rm -r [file-name.txt]`        | Remove a file (or folder)                              |
| `git rm -r --cached [folde-rname]` | Remove cached file (or folder)                         |
| `git reset <file>`                 | Reset a specific file or files to their previous state |

---

### Branching & Merging

| Command                                              | Description                                             |
| ---------------------------------------------------- | ------------------------------------------------------- |
| `git branch`                                         | List branches (the asterisk denotes the current branch) |
| `git branch -a`                                      | List all branches (local and remote)                    |
| `git branch [branch name]`                           | Create a new branch                                     |
| `git branch -d [branch name]`                        | Delete a branch                                         |
| `git push origin --delete [branch name]`             | Delete a remote branch                                  |
| `git checkout -b [branch name]`                      | Create a new branch and switch to it                    |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it                  |
| `git branch -m [old branch name] [new branch name]`  | Rename a local branch                                   |
| `git checkout [branch name]`                         | Switch to a branch                                      |
| `git checkout -`                                     | Switch to the branch last checked out                   |
| `git checkout -- [file-name.txt]`                    | Discard changes to a file                               |
| `git merge [branch name]`                            | Merge a branch into the active branch                   |
| `git merge [source branch] [target branch]`          | Merge a branch into a target branch                     |
| `git stash`                                          | Stash changes in a dirty working directory              |
| `git stash clear`                                    | Remove all stashed entries                              |

---

### Sharing & Updating Projects

| Command                                                                           | Description                                                 |
| --------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| `git push origin [branch name]`                                                   | Push a branch to your remote repository                     |
| `git push -u origin [branch name]`                                                | Push changes to remote repository (and remember the branch) |
| `git push`                                                                        | Push changes to remote repository (remembered branch)       |
| `git push origin --delete [branch name]`                                          | Delete a remote branch                                      |
| `git pull`                                                                        | Update local repository to the newest commit                |
| `git pull origin [branch name]`                                                   | Pull changes from remote repository                         |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git`     | Add a remote repository                                     |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH                     |

---

### Inspection & Comparison

| Command                                    | Description                    |
| ------------------------------------------ | ------------------------------ |
| `git log`                                  | View changes                   |
| `git log --summary`                        | View changes (detailed)        |
| `git log --oneline`                        | View changes (briefly)         |
| `git diff [source branch] [target branch]` | Preview changes before merging |

---
