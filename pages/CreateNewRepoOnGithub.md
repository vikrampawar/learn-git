>[Common Home](../README.md)
 
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
 

 
>[Common Home](../README.md)