>[Common Home](../README.md)
 
# Git Commands from Notion
 
- [Git Commands from Notion](#git-commands-from-notion)
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



 
>[Common Home](../README.md)