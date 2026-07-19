
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

```
rm -rf .git
```
>To delete .git folder

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
git commit -m "<Commit Message>"
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

**Wildcards in .gitignore**
>.gitignore supports pattern matching, so you don't have to list every file individually.
 
```
*.log
```
>Ignores every file ending in `.log`, no matter where it is in the project.
 
```
*.txt
!important.txt
```
>Ignores all `.txt` files, except `important.txt` — the `!` un-ignores a specific match.
 
```
build/
```
>Ignores an entire folder named `build`, wherever it appears.
 
```
/dist
```
>The leading `/` restricts this to only the `dist` folder at the project root, not any `dist` folder nested deeper in the project.
 
```
temp?.txt
```
>The `?` matches exactly one character — this ignores `temp1.txt`, `tempA.txt`, but not `temp10.txt`.

```
touch .gitkeep
```
>A .gitkeep file tracks the folder which wants to be tracked.

>Used to track Empty Directories.

--- 
## 🔍 Changes between Commits and Staging Area
After Staging,Modifying the repository will show it as `not staged` although git `status` is used to compare
```
git diff
```
>It compares current working directory and staging area.

```
git diff --staged
```
>Compares the previous commit and staged area.

>For example:
```
-Hello guys(removed)
+Hello guys i am Ayaan(Added)
```
---
## ⚡ Skipping Staging Area
To skip staging area and directly commit

```
git commit -a -m "<Direct Commit>"
```
>It adds and commits directly.

>Untracked files(new files/folders that haven't been staged) are not committed

>Does not add new files.

---
## 🔀 Moving and Renaming Files
Untracking a file by moving it or deleting it and Renaming the file without changing to the Desktop 

```
git rm --cached <File name>
```
>Untracks the File.

>Add the file in .gitignore and untracking it,since git has internally tracked the file or folder before.

```
git mv <old File name> <Current File name>
```
>renames the file and also stages it.

>Can be Checked through `git status`.

---




