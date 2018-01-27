# Git Pull Workflow

Refer to the following document when interacting with GitHub.

## Pull Reference

The syntax for pull mirrors that of push.

```bash
git pull origin master
```

To pull from GitHub to a branch _other than master_, we simply **checkout** and **specify the branch**.

```bash
git checkout other_branch
git pull origin other_branch
```

To simultaneously pull and merge most recent version of master into the branch you're currently on, simply pull from `origin/master` while on `origin master` _into_ `<other_branch>`.

```bash
git checkout other_branch
git pull origin master
```

This checks out `other_branch`; fetches changes to `master` from GitHub; and then merges them into `other_branch`.

In order to avoid issues with merge conflicts, you should always `git pull` before merging or pushing.

```bash
git checkout master
# Do some work, add, commit

git push origin master
git checkout other_branch
# Do some work, add commit

git checkout master
git pull
git merge other_branch
git push master
```
