**GIT CHEAT SHEET**

**SETUP**

Configuring user information used across all local repositories

| Command                                              | Description                                                            |
|------------------------------------------------------|------------------------------------------------------------------------|
| git config --global user.name “[firstname lastname]” | set a name that is identifiable for credit when review version history |
| git config --global user.email “[valid-email]”       | set an email address that will be associated with each history marker  |
| git config --global color.ui auto                    | set automatic command line coloring for Git for easy reviewing         |


**SETUP & INIT**

Configuring user information, initializing and cloning repositories

| Command         | Description                                                  |
|-----------------|--------------------------------------------------------------|
| git init        | initialize an existing directory as a Git repository         |
| git clone [url] | retrieve an entire repository from a hosted location via URL |


**STAGE & SNAPSHOT**

Working with snapshots and the Git staging area

| Command                               | Description                                                           |
|---------------------------------------|-----------------------------------------------------------------------|
| git status                            | show modified files in working directory, staged for your next commit |
| git add [file]                        | add a file as it looks now to your next commit (stage)                |
| git reset [file]                      | unstage a file while retaining the changes in working directory       |
| git diff                              | diff of what is changed but not staged                                |
| git diff --staged                     | diff of what is staged but not yet commited                           |
| git commit -m “[descriptive message]” | commit your staged content as a new commit snapshot                   |


**BRANCH & MERGE**

Isolating work in branches, changing context, and integrating changes

| Command                                            | Description                                             |
|----------------------------------------------------|---------------------------------------------------------|
| git branch                                         | List branches (the asterisk denotes the current branch) |
| git branch -a                                      | List all branches (local and remote)                    |
| git branch [branch name]                           | Create a new branch                                     |
| git branch -d [branch name]                        | Delete a branch                                         |
| git push origin --delete [branch name]             | Delete a remote branch                                  |
| git checkout -b [branch name]                      | Create a new branch and switch to it                    |
| git checkout -b [branch name] origin/[branch name] | Clone a remote branch and switch to it                  |
| git branch -m [old branch name] [new branch name]  | Rename a local branch                                   |
| git checkout [branch name]                         | Switch to a branch                                      |
| git checkout -                                     | Switch to the branch last checked out                   |
| git checkout -- [file-name.txt]                    | Discard changes to a file                               |
| git merge [branch name]                            | Merge a branch into the active branch                   |
| git merge [source branch] [target branch]          | Merge a branch into a target branch                     |
| git stash                                          | Stash changes in a dirty working directory              |
| git stash clear                                    | Remove all stashed entries                              |
| git stash pop                                      | Apply latest stash to working directory                 |


**Sharing & Updating Projects**

Retrieving updates from another repository and updating local repos

| Command                                                                         | Description                                                 |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|
| git push origin [branch name]                                                   | Push a branch to your remote repository                     |
| git push -u origin [branch name]                                                | Push changes to remote repository (and remember the branch) |
| git push                                                                        | Push changes to remote repository (remembered branch)       |
| git push origin --delete [branch name]                                          | Delete a remote branch                                      |
| git pull                                                                        | Update local repository to the newest commit                |
| git pull origin [branch name]                                                   | Pull changes from remote repository                         |
| git remote add origin ssh://git@github.com/[username]/[repository-name].git     | Add a remote repository                                     |
| git remote set-url origin ssh://git@github.com/[username]/[repository-name].git | Set a repository's origin branch to SSH                     |


**INSPECT & COMPARE**

Examining logs, diffs and object information

| Command                                  | Description                    |
|------------------------------------------|--------------------------------|
| git log                                  | View changes                   |
| git log --summary                        | View changes (detailed)        |
| git log --oneline                        | View changes (briefly)         |
| git diff [source branch] [target branch] | Preview changes before merging |
