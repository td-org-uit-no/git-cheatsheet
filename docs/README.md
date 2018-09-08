
<style>
	code    {
		width: auto;
		color: #b5e853;
			}
	body	{
		background-color: #000
			}
</style>

## Basic knowledge
* To move around with the use of the terminal a few commands are neccessary
  * cd
```sh
cd 				// Moves you to the home directory
cd .. 				// Moves you to the one directory out (Parent directory)
cd <DIRECTORY NAME>		// Moves you into directory
```
  * ls
```sh
ls				// Lists the directory contents
```
  * mkdir
```sh
mkdir <DIRECTORY NAME> 		// Creates a directory (folder) at current location
```

<hr> 

## Basic usage
* Initializing a git repository
```sh
git init
```
* Cloning an existing repository <br>
Most common is to clone a remote repository (From the interwebz)
```sh
git clone <REPOSITORY>
```
* Pulling all new changes from the remote
```sh
git pull
```

* Displaying git status <br>
This will display all changed files, which head, as well as other information about your current git status
```sh
git status
```

* Staging files
```sh
git add [PATH]			// Stages a single file or directory
git add . 			// Adds all changed files and untracked in all sub-directories
git add -a 			// Adds all tracked files that are changed 
```
* Committing files
```sh
git commit
git commit -m "MESSAGE" 	//Quick committing with short message
```
* Pushing all committed changes to the remote
```sh
git push
git push -f 			// Force pushes the commits. Allows for altering history (CARE)
```
```sh
git reset 			// Unstages all files
git reset --hard		// Resets all files back to HEAD
git reset HEAD~<NUMBER> --hard	// Resets ALL files and commits back <NUMBER> commits
git reset HEAD~<NUMBER> 	// Moves head back <NUMBER> commits, but maintains files changed
```
* Help
```sh
man git 			// Shows the manual entries  of git 
git <ANY COMMAND> -h 		// Shows the help entry for any given command
git help everyday 		//Shows a short list of everyday git commands
```
<hr>

## More advanced usage
* Branches
```sh
git branch 			// Lists local branches
git branch -a 			// Lists local branches & remote tracked branches
git branch -d 			// Deletes a fully merged branch
git branch -D <BRANCH NAME>		// Deletes branch even if it is not merged
git branch <BRANCH NAME> 	// Creates a new local branch
git checkout <BRANCH NAME> 	// Checks out a branch (Switches to branch)
```

* Stashing
 * Stashing is used to save changes that you would like to keep "in memory" but not commit. You can stash changes made, and reapply them at any later time. Very useful if you've made some messy changes, and you would like to switch branches, or work on something else.

```sh
git stash 		// Stashes all changed files
git stash list 		// Lists all the stashes
git stash show  	// Shows changes within stashes (*)
git stash apply		// Applies the stashed changes (*)
```
 * **\*** Stashes are saved separate, and can be shown/listed/applied separate by appending a ```stash@{NUMBER}``` onto those commands

<hr>
* Unfinished descriptions of other commands
```sh
git clean
git rebase
git fetch
git checkout
```
<hr>

## Personal favourites
```sh
git commit -a --amend --no-edit 	// Adds and amends changes to the last commit
git checkout -b <branch> 		// Shortcut for creating and checking out a new branch
git blame <FILENAME>			// Shows file with log of who committed which line
```
### Pretty git log?
Do you want that pretty pretty log instead of the bulky old one?<br>
It looks like this (With slightly more color)
```sh
* 7b84c86 - (HEAD -> master) Her er en commit (16 hours ago) <Jon Johansen>
* 9c21d09 - (origin/master, origin/HEAD) Add git lg alias command. (3 days ago) <Jon Johansen>
* 67f87f8 - Fix comment spacing (4 days ago) <Jon Johansen>
* c2e4573 - Add a few more descriptions (4 days ago) <Jon Johansen>
* 0575e8f - Testing theme (4 days ago) <Jon Johansen>
*   9770331 - Init github pages (7 days ago) <Jon Johansen>
|\
| * 01442b9 - Set theme jekyll-theme-hacker (7 days ago) <Jon Johansen>
* | e697e75 - Init gitignore and github pages (7 days ago) <Jon Johansen>
|/
* 6523eae - Init / Add readme (7 days ago) <Jon Johansen>
```
* To get the log you have to create an alias. 
  * To create the alias, simply copy paste this into your terminal:

```sh
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --"
```
* And to use it with your newly created alias
```sh
git lg 				//git lg is a custom alias you can create for log
```

Source: [Pretty git Log](http://garmoncheg.blogspot.com/2012/06/pretty-git-log.html)
<hr>

## Other great resources
* [Adding an existing project to GitHub using the command line](https://help.github.com/articles/adding-an-existing-project-to-github-using-the-command-line/)
* [Github For The Rest Of Us (Video)](https://www.youtube.com/watch?v=8_mHSdCkv3s)
* [How to undo (almost) anything with Git](https://blog.github.com/2015-06-08-how-to-undo-almost-anything-with-git/)
* [Learn Git Branching](https://learngitbranching.js.org/)
* [Oh, shit, git!](http://ohshitgit.com/)

## Anything missing? 
Feel free to create a pull request to the repository [HERE](https://github.com/jonjohansen/git-cheatsheet/pulls)
