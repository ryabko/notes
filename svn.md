Get list of branches
```
svn ls ^/project/branches
```

5 last commits
```
svn update
svn log --limit 5
```

Swith to the branch
```
svn switch ^/project/branches/1.2.1
```

Merge one commit from another branch
```
svn merge -c r155006 ^/project/branches/dev
```

Get svn prop
```
svn propget svn:mergeinfo
```

Feature branch
```
Create a new branch
svn copy ^/project/branches/dev ^/project/branches/TICKET-ID -m "TICKET-ID Created a branch"
svn switch ^/project/branches/TICKET-ID
As often as possible integrate changes from dev branch into the feature branch
svn switch ^/project/branches/TICKET-ID
svn update
svn merge ^/project/branches/dev
<commit>
Create a patch:
svn diff ^/project/branches/dev ^/project/branches/TICKET-ID > TICKET-ID.patch
Integrate everything into dev
svn switch ^/project/branches/dev
svn merge --reintegrate ^/project/branches/TICKET-ID
<commit>
Remove the branch
svn delete ^/project/branches/TICKET-ID -m "Removing an obsolete branch TICKET-ID"
```