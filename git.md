# Config
## edit git config
```bash
git config --global --edit
```
## Aliases
```bash
git config --global alias.co checkout
```
# Remotes
## add a remote
```bash
git remote add origin https://github.com/user/repo.git
```
# Commits
## git commit ignore post commit hooks like 'husky'
```bash
git commit --no-verify
```

# Branches
## git move branch (renaming)
[see this answer](https://stackoverflow.com/a/6591218/3073819)

# Resets
## squash last 3 commits mit wiederverwendung der commit-message
```bash
git reset --soft HEAD~3 && git commit --edit -m"$(git log --format=%B --reverse HEAD..HEAD@{1})"
```

## git soft reset X-Commits zurück (3 ist Variabel)
```bash
git reset --soft HEAD~3
```

# Restore
## restore einer File auf einen konkreten commit
```bash
git restore --source=<Commit-like> <Dateipfad>
```

# Rebase
## git rebase until last commit (sqash) (pre-remote)
```bash
git rebase -i <Commit vor den zu bearbeitenden>
```

## git rebase inetractive onto
```bash
git rebase -i --onto=origin/<Base> <Commit vor dem ältesten zu rebasenden>
```

## git rebase branch from the last merge-point.
```bash 
git rebase -i --onto=origin/<branch-to-rebase-with> $(git merge-base <actual-local-branch> <branch-to-rebase-with>)
```

## Squashing
[see how it works](https://www.internalpointers.com/post/squash-commits-into-one-git)

# Log
## get all log messages since (HEAD~#) # = count commits back
```bash
git log --format=%B HEAD~2..HEAD | uniq | grep -v '^$'
 ```

# Tagging
Add and Push annotated tag
```bash
git tag -a tagname -m "commit msg"
git push origin tagname
```
