# Git commands cheat sheet 
Git is a version control system that allows users to track and save changes through out their file-system. It is commonly associated with code versioning through websites like [github](www.github.com) and [gitlab](www.gitlab.com). 

## $ git init
```bash
# git init [repository-name]
git init git-repo
```
This creates a new 'empty' git repository called "git-repo".  When you specify the name of the repository, it will create a folder by that name inside of the current working directory. Withing the repository's folder a `.git` directory is created that holds git repository metadata required by git. 

## $ git status
```bash
git status
```
Returns the 'status' of the repository. The following information will be displayed: current branch, commits, untracked files. 

## $ git add
```bash
# git add [file-name]
git add message.txt
```
Adds files to the current commit we are working on.  It also accepts changes to a file. 

## $ git config
```bash
git config --global user.name "User's full name"
git config --global user.email "User's email address"
```

## $ git commit
```bash
git commit -m "Initial commmit message"
```
Git commit doesn't send the changes to a package repository manager, however, it is still useful for local version control. 

## $ git diff
```bash
# git diff [file-name]
git diff message.txt
```
Shows lines added, removed and modified for the file specified. 

## $ git clone 
```bash
# git clone [https-link]
git clone https://github.com/zmproni/obsidian-docs.git
```

## $ git reset -hard
```bash
git reset -hard
```

## $ git clean -fxd
```bash
git clean -fxd
```