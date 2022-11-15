>[Common Home](../README.md)
 
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


 
>[Common Home](../README.md)