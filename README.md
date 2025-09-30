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
### Create remote branch
```
git push origin branch-01
```
### Create new local branch linked to an existing remote branch
```
git checkout -b branch-01 origin/branch-01
```
### Link current local branch to remote branch
```
git push --set-upstream origin branch01
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
