>[Common Home](../README.md)
 
# Git Commands 

## What is the page about?

All the git commands that I use.

## Git log

### Show the last 10 commits

```bash
git log -10
```

### Show the last 10 commits with the diff

```bash
git log -10 -p
```

### Show the log in a single line

```bash
git log --pretty=oneline
``` 
 
### Show the log in a single line with the diff

```bash
git log --pretty=oneline -p
```
### What is a good commit message?

```bash
git log --pretty=oneline --abbrev-commit
```

### git command to draw a graph

```bash
git log --graph --oneline --all
```


git remote set-url origin git@github.com:USERNAME/REPOSITORY.git
find . -type d -name .git -exec sh -c "cd \"{}\"/../ && pwd && git status" \;






 

 
>[Common Home](../README.md)