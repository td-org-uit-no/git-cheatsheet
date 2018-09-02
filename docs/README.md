
<style>
	code    {
		width: auto;
		color: #b5e853;
			}
	body	{
		background-color: #000
			}
</style>

## Introduction
This is a small cheatsheet containing the basics needed on a day-to-day basis with git.


### Basic knowledge
  * cd
```shell
cd 				// Moves you to the home directory
cd .. 				// Moves you to the one directory out (Parent directory)
cd <DIRECTORY NAME>		// Moves you into directory
```
  * ls
```shell
ls				// Lists the directory contents
```
  * mkdir
```shell
mkdir <DIRECTORY NAME> 		// Creates a directory (folder) at current location
```

<hr> 

## Basic usage
* Initializing a git repository
```shell
git init
```
* Cloning an existing repository <br>
Most common is to clone a remote repository (From the interwebz)
```shell
git clone <REPOSITORY>
```
* Pulling all new changes from the remote
```shell
git pull
```

* Displaying git status <br>
This will display all changed files, which head, as well as other information about your current git status
```shell
git status
```

* Staging files
```shell
git add [PATH]			// Stages a single file or directory
git add . 			// Adds all changed files and untracked in all sub-directories
git add -a 			// Adds all tracked files that are changed 
```
* Committing files
```shell
git commit
git commit -m "MESSAGE" 	//Quick committing with short message
```
* Pushing all committed changes to the remote
```shell
git push
git push -f 			// Force pushes the commits. Allows for altering history (CARE)
```
<hr>

## More advanced usage
* Branches
```shell
git branch 			// Displaying local branches
```
* Other
```shell
git rebase
git reset
git stash
git fetch
git checkout
git help everyday
```
<hr>

## Personal favourites
```shell
git commit -a --amend --no-edit 	//Adds and amends changes to the last commit
git checkout -b <branch> // Shortcut for creating and checking out a new branch
```
### Pretty git log?
```shell
git lg 				//git lg is a custom alias you can create for log
```
* To create the alias, copy paste this into your terminal:

```shell
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --"
```
Source: [Pretty git Log](http://garmoncheg.blogspot.com/2012/06/pretty-git-log.html)
<hr>

## Other great resources

* [Github For The Rest Of Us (Video)](https://www.youtube.com/watch?v=8_mHSdCkv3s)
* [How to undo (almost) anything with Git](https://blog.github.com/2015-06-08-how-to-undo-almost-anything-with-git/)
* [Learn Git Branching](https://learngitbranching.js.org/)
