# Useful git commands

List of useful git commands I frequently need to use and forget

&nbsp;

## Config
### List git configs
```
git config --local --list
cat .\.git\config
```
```
git config --global --list
```
### Set user name and email
```
git config --local user.name "John Doe"
git config --global user.name "John Doe"
```
```
git config --local user.email "john.doe@mail.com"
git config --global user.email "john.doe@mail.com"
```
### Set default editor
```
git config --global core.editor vim
git config --global core.editor "code --wait"
```

&nbsp;

## Log
### Log commits in one line
```
git log -5 --oneline
```

&nbsp;

## Branch
### Change default branch name
```
git branch -M main
```
### Push local branch that does not exists on remote yet
```
git push -u origin branch-name
```

&nbsp;

## HEAD

### Move HEAD to a specific commit id (detached HEAD state)
```
git checkout <commit-id>
```

### Go back to the last branch commit
```
git switch -
```

&nbsp;

## Rebase

### Rebase the last 3 commits (HEAD commit + previous 2)
```
git rebase -i HEAD~3
```

### Cancel rebase process
```
git rebase --abort
```
