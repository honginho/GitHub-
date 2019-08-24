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
git push origin master:<branch_name>
```

### Switch to master or branch
```shell
# switch to master (two ways)
git checkout -       # 1st
git checkout master  # 2nd

# switch to specific branch
git checkout <specific_branch>
```

### Discard changes in working directory
```shell
git checkout -- <file>
```

### (On branch) Revert back to the specific commit and start new commit from it
```shell
# check every commit
git log --oneline

# revert back to the specific commit
git checkout <specific_commit_hash>

# if accidentally modify something at this moment
# it is impossible to revert the latest commit
# so force to switch to the latest commit
# and revert back to the specific commit again
git checkout -f -
git checkout <specific_commit_hash>

# remove the latest commit
git revert <latest_commit_hash>

# -----------------------------
#  do something for new commit
# -----------------------------

# COMMIT step
git add .
git commit -m "<commit_details>"

# PUSH step
git push origin master:<branch_name> -f
```