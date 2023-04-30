>[Common Home](../README.md)
 
# Git Page
 
- [Git Page](#git-page)
  - [Basic git commmands](#basic-git-commmands)
  - [Add and commit in a one got](#add-and-commit-in-a-one-got)
  - [Stash : Save with a name](#stash--save-with-a-name)
  - [Stash : Get a particular stash](#stash--get-a-particular-stash)
  - [Show : the changes made in a particular commit](#show--the-changes-made-in-a-particular-commit)
  - [Diff : See the changes made in a particular commit](#diff--see-the-changes-made-in-a-particular-commit)
  - [Show global git configuration](#show-global-git-configuration)
    - [Update Configuration set auto crlf](#update-configuration-set-auto-crlf)
    - [Rename a folder](#rename-a-folder)
  - [Miscellaneous](#miscellaneous)
    - [Mac credentials setup](#mac-credentials-setup)
- [](#)
- [Git Commands](#git-commands)
  - [What is the page about?](#what-is-the-page-about)
  - [Git log](#git-log)
    - [Show the last 10 commits](#show-the-last-10-commits)
    - [Show the last 10 commits with the diff](#show-the-last-10-commits-with-the-diff)
    - [Show the log in a single line](#show-the-log-in-a-single-line)
    - [Show the log in a single line with the diff](#show-the-log-in-a-single-line-with-the-diff)
    - [What is a good commit message?](#what-is-a-good-commit-message)
    - [git command to draw a graph](#git-command-to-draw-a-graph)
- [Git Cheatsheet created by PawarV](#git-cheatsheet-created-by-pawarv)
  - [How to do the intial commit](#how-to-do-the-intial-commit)
  - [How to create the same repo in both Github and Bitbucket.](#how-to-create-the-same-repo-in-both-github-and-bitbucket)
    - [textfiles](#textfiles)
- [Creating a new repository on Github](#creating-a-new-repository-on-github)
  - [How to set the author of a repository different the global settings?](#how-to-set-the-author-of-a-repository-different-the-global-settings)
- [Git Notes](#git-notes)
  - [Commands](#commands)
    - [Show Configuration](#show-configuration)
    - [Update Configuration](#update-configuration)
    - [Rename a folder](#rename-a-folder-1)
  - [Q) How to use git on IMac](#q-how-to-use-git-on-imac)
  - [Git access key chain](#git-access-key-chain)


## Basic git commmands

`git show` Shows the changes done in the last commit

`git status` Shows modified files, an d and only directories of untracked files.

`git status -u=name` Shows the same output as above.

`git status -u` shows untracked files

`git push --set-upstream origin <branch_name>` Create current branch on remote

`git checkout master` Switch to master branch

`git merge <branch_name>` Merge the branch into the current branch

`git push` Push the current branch to remote

`git pull` Get all commits from remote to local for the current branch


## Add and commit in a one got

```sql
git commit -a -m "Initial commit"
```

## Stash : Save with a name

From [https://devconnected.com/how-to-git-stash-changes/#:~:text=In order to create a git stash with,but it assigned a custom name to it](https://devconnected.com/how-to-git-stash-changes/#:~:text=In%20order%20to%20create%20a%20git%20stash%20with,but%20it%20assigned%20a%20custom%20name%20to%20it).

Saving with a name 

```bash
git stash save "some_name"
```

Listing the stashes

```bash
git stash list
```

## Stash : Get a particular stash

Getting back a particular stash (applying)

```bash
git stash apply stash@{0}  // the last stash
git stash apply            // the last stash
git stash apply stash@{1}  // the last but one stash
```

## Show : the changes made in a particular commit 


`git show 7d3d630cdd5d4f7961a0a5cf8c6098828b7150d8`


## Diff : See the changes made in a particular commit 


`git diff COMMIT_HASH~ COMMT_HASH`


## Show global git configuration

`git config --global -l`

`git config --list  # show all config (~/.gitconfig)`

### Update Configuration set auto crlf 

```bash
git config --global -e    (opens up editor)
git config --global core.autocrlf true
```

### Rename a folder

```bash
git mv DSProductExtractAdobe tmp
git mv tmp DsProductExtractAdobe
```

## Miscellaneous

### Mac credentials setup

If Git asks for your password every time you push a commit, it means it has lost access to password key chain. The below sets up Git to access the key chain for password.

```bash 
git config --global credential.helper osxkeychain
```

# 
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




```sh

find . -type d -name .git -exec sh -c "cd \"{}\"/../ && pwd && git status" \;


# set origin
git remote set-url origin git@github.com:USERNAME/REPOSITORY.git

# delete the current url setting
git remote set-url  --delete origin  https://github.com/rumq/Kafka-Streams-with-Spring-Cloud-Stream.git
# add the new url setting
git remote set-url  --add origin  git@github.com:rumq/Kafka-Streams-with-Spring-Cloud-Stream.git


```

```sh
# use git instead of https
git remote set-url origin git@github.com:USERNAME/REPOSITORY.git

git remote -v
git remote set-url origin git@github.com:rumq/designpatterns.git
git st



```

# Git Cheatsheet created by PawarV

Command                            			| Description               			| Options
------------                				| -------------             			| -------------
`git log `                  				| Show log                  			| `--stat` with statistics
`git version`               				| Show verion of git        			|
`git config`                				| Show and update config    			| `--global color.ui auto` <br></br> `--global http.sslVerify false`  <br> `--global core.editor <editor>` <br> `--global push.defaul upstream` Pushes to upstream udacity suggestion<br> '-- global merge.conflictstyle diff3` udacity suggestion <br> `--global core.excludesfile ~/.gitignore_global`
`git branch <branch>`       				| Create a branch           			|
`git checkout <branch>`     				| Switch to a branch        			| `-- .` delete untracked files
`git symbolic-ref --short HEAD`         	| Get the name of current branch 		|
`git push --set-upstream origin <branch>` 	| Push local branch to remote           |
`git clean`                             	| delete untracked files    			| `-n` check which files <br> `-f` to force delete
`git log -p filename`                   	| generate patches of each log entry 	|
`git reset HEAD~`                       	| undo last commit                      |

 

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

# Creating a new repository on Github
 
First create a new empty repository on github.

Then create a new repository on my box.

```bash
# Create the project folder
mkdir ~/git/crypto
cd ~/git/crypto
# Initialize the git reposiorty
git init
# Create a file
echo "#crypto " >> README.md
# Add the file to git
git add README.md
# Make the first commit
git commit -m "first commit"
# Move the current branch to main 
git branch -M main
# Add the gihub url as the remote
git remote add origin https://github.com/vikrampawar/crypto.git
# push the main branch to origin
git push -u origin main

```

## How to set the author of a repository different the global settings?

Check the global settings.

```bash
git config --list  # show all config (~/.gitconfig)

```

# Git Notes


## Commands

### Show Configuration
git config --global -l 

### Update Configuration 
git config --global -e    (opens up editor)
git config --global core.autocrlf true

### Rename a folder

git mv DSProductExtractAdobe tmp
git mv tmp DsProductExtractAdobe



## Q) How to use git on IMac

1. Make changes to files
2. Add the files to staging by git add .
3. Commit the files using git commit.
4. Push the changes to master using git push.



## Git access key chain

If Git asks for your password every time you push a commit, it means it has lost access to password key chain. The below sets up Git to access the key chain for password.

```bash 
git config --global credential.helper osxkeychain
```

>[Common Home](../README.md)