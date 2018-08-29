
<style>
	code    {
		max-width: 600px;
		color: #b5e853;
			}
</style>

# git cheatsheet
<hr>

## Introduction
This is a small cheatsheet containing the basics needed on a day-to-day basis with git. 

### Basic useful terminal commandos

  * cd
```shell
cd 				//Moves you to the home directory
cd .. 				//Moves you to the one directory out (Parent directory)
cd <DIRECTORY NAME>		//Moves you into directory
```
  * ls
```shell
ls				//Lists the directory contents
```
  * mkdir
```shell
mkdir <DIRECTORY NAME> 		//Creates a directory (folder) at current location
```

<hr> 

## Basic usage
* Initializing a git repository
```shell
git init
```
* Cloning an existing repository
Most common is to clone a remote repository (From the interwebz)
```shell
git clone <REPOSITORY>
```
* Displaying git status
This will display all changed files, which head, as well as other information about your current git status
```shell
git status
```

* Staging files
```shell
git add [FILE PATH]
git add . 			// Adds all changed files and untracked files subfolder from current folder
git add -a 			// Adds all tracked files that are changed 
```
* Committing files
```shell
git commit
git commit -m "MESSAGE" 	//Quick committing with short message
```
* Displaying git status
```shell
git status
```
* Displaying git status
```shell
git status
```
* Other
```shell
git commit --amend --no-edit
git reset
git stash
git log PRETTYLOG?
git clone
git pull
git fetch
git checkout
git branch
git status
git push
git rebase
```

<hr>

## Other great resources

* [Github For The Rest Of Us (Video)](https://www.youtube.com/watch?v=8_mHSdCkv3s)
* [How to undo (almost) anything with Git](https://blog.github.com/2015-06-08-how-to-undo-almost-anything-with-git/)
* [Learn Git Branching](https://learngitbranching.js.org/)

<hr>
### Thanks to..
* [Max Johansen](https://github.com/MaxJohansen)