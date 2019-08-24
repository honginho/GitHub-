# Learn how to git

### Create branch to Github
```shell
# clone target repo first and move to the directory
git clone <target_repo>
cd <target_repo_dir>

# create a branch
git checkout -b <branch_name>

# --------------
#  do something
# --------------

# COMMIT step
git add .
git commit -m "<commit_details>"

# PUSH step
git push origin <branch_name>
```

### Switch to master or branch
```shell
# switch to master
git checkout master

# switch to specific branch
git checkout <specific_branch>
```

### Discard changes
```shell
# before add command
git checkout -- <file>

# before commit, after add command
git reset
git checkout -- <file>
```

### (On branch) Revert back to the specific commit and start new commit from it
```shell
# check every commit
git log --oneline

# revert back to the specific commit
git checkout <specific_commit_hash>

# remove the latest commit
git revert <latest_commit_hash>

# -----------------------------
#  do something for new commit
# -----------------------------

# COMMIT step
# if change something ......
git add .
git commit -m "<commit_details>"
# else ......
git commit -a

# PUSH step
git push origin HEAD:<branch_name> -f

# --------------------------------------------------
#  however, HEAD detached at <detached_commit_hash>
# --------------------------------------------------

# check branch
git branch # || git branch -v

# create a temp branch for the detached HEAD
git branch <tmp_branch_name> <detached_commit_hash>

# checkout and merge temp branch to original branch
git checkout <branch_name>
git merge <tmp_branch_name>

# after resolve conflict parts
git add .
git commit -m "<commit_details>"
git push origin <branch_name>
```
