Show current branch
```
git branch
```

Show all branches
```
git branch -a
```

Switch to branch
```
git checkout branch-name
```

Create a feature branch and switch to it
```
git checkout -b feature-branch
```

Push branch to the origin repository
```
git push -u origin feature-branch
```

Delete a local branch
```
git branch -d branch_name
```

Delete a remote branch
```
git push origin --delete branch_name
```

Refresh list of remote branches
```
git remote update origin --prune
```

Rebase
```
git checkout development
git pull origin development
git checkout feature-branch
git rebase development
```

Installing local git
https://www.digitalocean.com/community/tutorials/how-to-set-up-a-private-git-server-on-a-vps
```
ssh-keygen -C "<my-email>"
```

Ends of lines

Disable conversion
```
git config core.autocrlf false
```
On Linux
```
git config --global core.autocrlf input
```
On Windows
```
git config --global core.autocrlf true
```
Also, look at gitattributes file

Move last commit to another branch ssuming that the wrong commit is in local development.

Create a new branch from development branch (it will have all commits)
```
git branch new-branch
```
Remove the last commit from development branch
```
git reset --hard HEAD~1
```
Go to a new branch
```
git checkout new-branch
```