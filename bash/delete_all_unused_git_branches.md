# Delete unused git branches
To delete branches that have been merged, use the following:
```bash
git branch --merged | egrep -v "(^\*|master|dev)" | xargs git branch -d
```