> [Common Home](../README.md)

# Git Page

- [Git Page](#git-page)
- [Links](#links)
- [Git Commands](#git-commands)
  - [Basic git commands](#basic-git-commands)
  - [Advanced](#advanced)
  - [Git log](#git-log)
  - [Stash](#stash)
  - [Configuration](#configuration)
- [Git Cheatsheet](#git-cheatsheet)
- [Howtos](#howtos)
  - [How to do the intial commit](#how-to-do-the-intial-commit)
  - [How to create the same repo in both Github and Bitbucket.](#how-to-create-the-same-repo-in-both-github-and-bitbucket)
    - [Removing it from bitbucket](#removing-it-from-bitbucket)
  - [How to create a new repository on Github](#how-to-create-a-new-repository-on-github)
  - [How to setup access key chain](#how-to-setup-access-key-chain)
  - [How to recursively show status of git repos under a directory](#how-to-recursively-show-status-of-git-repos-under-a-directory)
  - [How to setup remote origin](#how-to-setup-remote-origin)


# Links

- [Git Cheatsheet](https://training.github.com/downloads/github-git-cheat-sheet/)
- [SCM Documentation](https://git-scm.com/docs/git-push)
- [SCM Documentation for git-push](https://git-scm.com/docs/git-push)
- [Create a Git stash with a name](https://devconnected.com/how-to-git-stash-changes/#:~:text=In%20order%20to%20create%20a%20git%20stash%20with,but%20it%20assigned%20a%20custom%20name%20to%20it).

# Git Commands

## Basic git commands

```sh
# Shows the changes done in the last commit
git show
# Show : the changes made in a particular commit
git show 7d3d630cdd5d4f7961a0a5cf8c6098828b7150d8
# Shows modified files, and and only directories of untracked files.
git status
# Create current branch on remote
git push --set-upstream origin <branch_name>`
# Switch to master branch
git checkout master
# Merge the branch into the current branch
git merge <branch_name>`
# Push the current branch to remote
git push
# Get all commits from remote to local for the current branch
git pull
# Add and commit in a one go
git commit -a -m "Initial commit"

# Diff : See the changes made in a particular commit
git diff COMMIT_HASH~ COMMT_HASH

# rename a file
git mv A B


```

## Advanced

## Git log

```sh
# Show the last 10 commits
git log -10
# Show the last 10 commits with the diff
git log -10 -p
# Show the log in a single line
git log --pretty=oneline
# Show the log in a single line with the diff
git log --pretty=oneline -p
# What is a good commit message?
git log --pretty=oneline --abbrev-commit
# git command to draw a graph
git log --graph --oneline --all
```

## Stash

```sh
# listing stashes
git stash list
# Get a particular stash
# Getting back a particular stash (applying)
git stash apply stash@{0}  # the last stash
git stash apply            # the last stash
git stash apply stash@{1}  # the last but one stash
# saving a stash
git stash save "some_name"
```

## Configuration

```sh
# Show All Configuration
git config --list  # show all config (~/.gitconfig)
# show global config
git config --global -l
## show author
git config --global --get user.name
# Update Configuration
git config --global -e    # (opens up editor)
# show core.autocrlf
git config --global --get core.autocrlf
# set core.autocrlf
git config --global core.autocrlf true

```

# Git Cheatsheet

See also [Git Cheatsheet](https://training.github.com/downloads/github-git-cheat-sheet/)

| Command                                   | Description                        | Options                                                                                                                                                                                                                                                                                             |
| ----------------------------------------- | ---------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `git log `                                | Show log                           | `--stat` with statistics                                                                                                                                                                                                                                                                            |
| `git version`                             | Show verion of git                 |
| `git config`                              | Show and update config             | `--global color.ui auto` <br></br> `--global http.sslVerify false` <br> `--global core.editor <editor>` <br> `--global push.defaul upstream` Pushes to upstream udacity suggestion<br> '-- global merge.conflictstyle diff3`udacity suggestion <br>`--global core.excludesfile ~/.gitignore_global` |
| `git branch <branch>`                     | Create a branch                    |
| `git checkout <branch>`                   | Switch to a branch                 | `-- .` delete untracked files                                                                                                                                                                                                                                                                       |
| `git symbolic-ref --short HEAD`           | Get the name of current branch     |
| `git push --set-upstream origin <branch>` | Push local branch to remote        |
| `git clean`                               | delete untracked files             | `-n` check which files <br> `-f` to force delete                                                                                                                                                                                                                                                    |
| `git log -p filename`                     | generate patches of each log entry |
| `git reset HEAD~`                         | undo last commit                   |

# Howtos

## How to do the intial commit

```bash
echo "# lispprojects" >> README.md
git init
git add README.md
git commit -m "first commit"
# arg1 name of the remote (origin)
# arg2 url that it represents
git remote add origin https://github.com/vikrampawar/lispprojects.git
# add upstream/tracking reference
git push -u origin master

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

### Removing it from bitbucket

I moved the repo to github. I first created the repository with the same name on github called `textfiles`.

```bash
#  add as one of the remotes.
git remote add github https://github.com/vikrampawar/textfiles.git
#  remove the bitbucket
git remote remove origin
```

## How to create a new repository on Github

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

## How to setup access key chain

If Git asks for your password every time you push a commit, it means it has lost access to password key chain. The below sets up Git to access the key chain for password.

```bash
git config --global credential.helper osxkeychain
```

## How to recursively show status of git repos under a directory

```sh
# Recursively find all git repos and show their status
find . -type d -name .git -exec sh -c "cd \"{}\"/../ && pwd && git status" \;
```

## How to setup remote origin

```sh
# Show the origin
git remote -v
# set origin (use git instead of https)
git remote set-url origin git@github.com:USERNAME/REPOSITORY.git
# delete the current url setting
git remote set-url  --delete origin  https://github.com/rumq/Kafka-Streams-with-Spring-Cloud-Stream.git
# add the new url setting
git remote set-url  --add origin  git@github.com:rumq/Kafka-Streams-with-Spring-Cloud-Stream.git

```

> [Common Home](../README.md)
