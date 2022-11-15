>[Common Home](../README.md)
 
# Initial Setup
 
This is the setup from the Udacity course [https://github.com/AnthonyMedina/Udacity-Git-Cheatsheet](https://github.com/AnthonyMedina/Udacity-Git-Cheatsheet)

Get colours from here [https://gist.github.com/vratiu/9780109](https://gist.github.com/vratiu/9780109)

## Git Setup

This setup is probably from the Udacity course on Git.

**Changing background color**

If you prefer the background color of Git Bash to be something other than black, you can change it in the "Defaults" menu under the "Colors" tab. If you like the background color as-is, you don't need to make any changes.

**Downloading necessary files** 

Save this file in your home directory with the name [git-completion.bash](https://raw.githubusercontent.com/git/git/master/contrib/completion/git-prompt.sh).

Save this file in your home directory with the name [git-prompt.sh](https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash).

Download bash_profile_course from the Downloadables section.

If you already have a file in your home directory named .bash_profile, copy the content from bash_profile_course and paste it at the bottom of .bash_profile. Otherwise, move bash_profile_course to your home directory and rename it to .bash_profile. (If you're curious to learn more about how bash prompts work, see this page.)

**Making Git configurations**

Run the following Git configuration commands. The first one will need to be modified if you are using a text editor other than Sublime, or if Sublime is installed in another location for you. See this page for the correct command for a couple of other popular text editors. For any other editor, you'll need to enter the command you use to launch that editor from Git Bash.

git config --global core.editor "'C:/Program Files/Sublime Text 2/sublime_text.exe' -n -w"
git config --global push.default upstream
git config --global merge.conflictstyle diff3

Make sure you can start your editor from Git Bash

If you use Sublime, you can do this by adding the following line to your .bash_profile:

alias subl="C:/Program\ Files/Sublime\ Text\ 2/sublime_text.exe"
Restart Git Bash
You'll need to close and re-open Git Bash before all your changes take effect.



 
>[Common Home](../README.md)