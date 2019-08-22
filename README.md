# Learn how to git

### Create branch to Github
```shell
  # clone target repo first and move to the directory
$ git clone <target_repo>
$ cd <target_repo_dir>

  # create a branch
$ git checkout -b <branch_name>

  # ----------------
  #   do something
  # ----------------

  # COMMIT step
$ git add .
$ git commit -m "<commit_details>"

  # PUSH step
$ git push origin HEAD:<branch_name>
```