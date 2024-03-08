# Git commands

List of Git commands to make life easier

&nbsp;

## Init local repository
```
git init
```

&nbsp;

## Config

### List git configs
```
git config --list
```

### List local user name end email values
```
git config user.name && git config user.email
```

### Set global name and email (all repos)
```
git config --global user.name "John Doe"
git config --global user.email john.doe@mail.com
```

## Set local name and email (just one repo)
```
git config user.name "John Doe"
git config user.email john.doe@mail.com
```

### Set default editor and merge tool
```
git config --global core.editor vim
git config --global merge.tool vimdiff
```

&nbsp;

## Remote

### Show remote urls
```
git remote -v
```

### Link local to remote repository
```
git remote add origin https://github.com/USERNAME/REPOSITORY-NAME.git
```

### Link local to remote repository with token for authentication
```
git remote add origin https://TOKEN@github.com/USERNAME/REPOSITORY-NAME.git
```

### Link local to remote repository with username and password for authentication
```
git remote add origin https://USERNAME:PASSWQRDgithub.com/USERNAME/REPOSITORY-NAME.git
```

### Show remote repository infos
```
git remote show origin
```

### Rename remote repository
```
git remote rename origin new-name
```

### Unlink remote repository
```
git remote rm origin
```

### Update active origin
```
git remote set-url origin (new url here)
```

&nbsp;

## Status
```
git status
```

&nbsp;

## Staging

### Stage file
```
git add someFile.txt
```

### Stage directory
```
git add someDirectory
```

### Stage all files
```
git add .
```

### Unstage all files
```
git reset
```

&nbsp;

## Commit

### Commit with one line message
```
git commit -m "my message"
```

### Commit with multiline message
```
git commit -m "title message
>
> this is the message body.
> press Enter do add more lines.
> here is the last line"
```

### Change last commit message
```
git commit --amend -m "New commit message"
git push --force
```

&nbsp;

## Push

### First push to main branch of a new empty remote repository
```
git push -u origin main
```

### Normal push
```
git push
```

&nbsp;

## Pull
```
git pull
```

&nbsp;

## Fetch

### Normal fetch
```
git fetch
```

### Fetch and prune (remove deleted remote branches)
```
git fetch -p
```

&nbsp;

## Clone
```
git clone https://github.com/USERNAME/REPOSITORY-NAME.git
```

&nbsp;

## Log

### Log last commit
```
git log -1
```
### Log last commit with more details
```
git log -1 --stat
```
### Log each commit in one line
```
git log --pretty=oneline
```
### Log file history
```
git log -- fileDirectory
```
### Exit log list
```
q
```

&nbsp;

## Branch

### Change default branch name
```
git branch -M main
```


### Show local branches
```
git branch
```
### Show remote branches
```
git branch -r
```
### Show local and remote branches
```
git branch -a
```
### Create new branch
```
git branch branch-01
```
### Change branch
```
git checkout branch-01
```
### Create and use new branch
```
git checkout -b branch-01
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
### Delete local branch
```
git branch -d branch-01
```
### Delete remote branch
```
git push origin -d branch-01
```

&nbsp;

## Merge

### Merge some branch to your current branch
```
git merge branch-01
```

&nbsp;

## Blame

### Show the last modification of a file within the given line range
```
git blame -L 1,10 (file-path)
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
