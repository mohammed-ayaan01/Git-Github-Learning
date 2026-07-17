
## 🖥️ Basic Commands in Git
A few basic terminal commands i personally use in git bash for navigating folders and files of my project

```
pwd
```
>It displays the present working directory.

```
cd 
```
>Changes to the home directory.

```
cd <Folder Name>
```
>Changes to a specified directory.

```
mkdir <Folder name>
```
>Creates a new directory with a name.

```
touch <File>
```
>Creates a new file with its extension.

```
ls 
```
>List the files and directories.

--- 
## 📦 Tracking a Project in Git
I track my project and get it ready to push in my git repository
```
git status
```
>To check the changes tracked,modified,staged and untracked files.

```
git init
```
>Initializes a new git repository.

```
git add -A 
```
>Stages all changes including deleted files.

```
git add .
```
>Stages all changes in the current working directory.

```
git commit -m "<Messege Committed>"
```
>Commit the changes from staging area to the git repository.

--- 

## 🌐 Cloning a Remote Git Repository
I clone repositories and enhance them or find issues

```
git clone <Link> 
```
>Clones a remote git repository.

```
git clone <Link> <name>
```
>Clones a remote git repository to a desired name.

--- 

## 🚫 .gitignore and .gitkeep
Ignoring a git folder 

```
touch .gitignore
```
>Creates a .gitignore file where other files and folders can be ignored and not tracked.


**Note**
>A .gitignore file can also ignore a file inside a folder.

>A Blank Folder is ignored and if it contains a ignored file,it ignores the whole folder.

```
touch .gitkeep
```
>A .gitkeep file tracks the folder which wants to be tracked.

>Used to track Empty Directories.

--- 




