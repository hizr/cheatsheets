# Config
## edit git config
```bash
git config --global --edit
```
## Aliases
```bash
git config --global alias.co checkout
```

# Commits
## git commit ignore post commit hooks like 'husky'
```bash
git commit --no-verify
```

# Resets
## squash last 3 commits mit wiederverwendung der commit-message
```bash
git reset --soft HEAD~3 && git commit --edit -m"$(git log --format=%B --reverse HEAD..HEAD@{1})"
```

## git soft reset X-Commits zurück (3 ist Variabel)
```bash
git reset --soft HEAD~3
```

# Rebase
## git rebase bis zum letzten commit (sqash) (pre-remote)
```bash
git rebase -i <Commit vor den zu bearbeitenden>
```

## git rebase inetractive onto
```bash
git rebase -i --onto=origin/<Base> <Commit vor dem ältesten zu rebasenden>
```

## git rebase branch ab den letzten Mergpunkt
```bash 
git rebase -i --onto=origin/<branch-to-rebase-with> $(git merge-base <actual-local-branch> <branch-to-rebase-with>)
```

# Log
## get all log messages since (HEAD~#) # = count commits back
```bash
git log --format=%B HEAD~2..HEAD | uniq | grep -v '^$'
 ```