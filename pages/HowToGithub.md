# Howto Github

## How to do the intial commit

```bash
echo "# lispprojects" >> README.md
git init
git add README.md
git commit -m "first commit"
# remote add command takes two arguments, name of the remote (origin)
# and the url that it represents
git remote add origin https://github.com/vikrampawar/lispprojects.git

# The -u ~ --set-upstream https://git-scm.com/docs/git-push 
# adds upstream/tracking reference
git push -u origin master
bash
```
if you are asking to login, user id is vikram.pawar@gmail.com and not vikrampawar.


## How to create the same repo in both Github and Bitbucket.

Read my own blogpost https://dev.to/vikrampawar/same-repo-on-both-bitbucket-and-github-jpa 

I have the project `javaprojects` on both github and bitbucket.

```bash
# it shows two remote urls, the fetch seems to be the same as any other git project.
git remote -v
remote.origin.url=https://Vikrampawar@bitbucket.org/Vikrampawar/javaprojects.git
remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*
remote.origin.url=https://github.com/vikrampawar/javaprojects.git

```

### textfiles
I moved the repo to github. I first created the repository with the same name on github called `textfiles`.


```bash
#  add as one of the remotes.
git remote add github https://github.com/vikrampawar/textfiles.git
#  remove the bitbucket
git remote remove origin
```


