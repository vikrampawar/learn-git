>[Common Home](../README.md)
 
# ProGit Book Notes Introduction
 
## Snapshots not differences

![Snapshots not differences](../assets/diagrams/SnapshotsVsChangesToFiles.png)

The whole repository is available locally.
So version history is a local call.

Files are stored as hash value of the files contents rather the name of the file.

Data is never delete, git only adds to the repository.
This makes it easy to go back in history.

## Git has three stages modified, staged and committed.

### files in modified state
Files have been modified and git had nothing to do with the changes.

### modifications staged
Files have been marked so the changes will go into git.


### staged modifications committed
Safely stored in the git repository

### Working Directory, Staging area, and Git directory

![Working Directory, Staging area, and Git directory](../assets/diagrams/WorkingTreeStagingAreaGitDirectory.png)


## Command line 

Some commands can only be run on command line.
They are installed on every system that has git.

## First time git setup

### See git config and the source of that config

`git config --list --show-origin`


### Setup user name and email

`git config --global user.name "Dharam Veer"`

`git config --global user.email dharam@kuru.com`

### Setup the editor

`git config --global core.editor emacs`

### Default branch name is **main**

 `git config --global init.defaultBranch main`

### Getting help

`get help <verb>`

`git <verb> --help`

### Git help IRC channels

 `#git, #github, or #gitlab`

### Git concise help

`git add -h`

# Git Basics

## Create a new repository

`git init`

## Clone a repository

`git clone <repo location>`

## Recording changes

The `tracked` files are the files that Git knows about, the rest are `untracked` files.

![LifeCycleOfFiles](../assets/diagrams/LifeCycleOfFiles.png)

## Checking status

See the current status of files `git status`

Create a file called `README` with some data in it `echo data > README`.

To track this new files `git add README`

## Staging modified files


 
>[Common Home](../README.md)