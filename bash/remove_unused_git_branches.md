# Remove unused or merged branches from local git

To list all merged branches:

```bash
git branch -a --merged
```

then, to remove all merged branches:

```bash
git branch -d $(git branch -a --merged)
```

Alternatively, if you cannot delete the branch, but are absolutely sure you want it gone:

```bash
git branch -D $(git branch -a --merged)
```
