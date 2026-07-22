
## 🖥️ Basic Commands in Git
A few basic terminal commands I personally use in Git Bash for navigating folders and files of my project

```bash
pwd
```
> It displays the present working directory.

```bash
cd 
```
> Changes to the home directory.

```bash
cd <Folder Name>
```
> Changes to a specified directory.

```bash
mkdir <Folder name>
```
> Creates a new directory with a name.

```bash
touch <File>
```
> Creates a new file with its extension.

```bash
ls 
```
> List the files and directories.

```bash
rm -rf .git
```
> To delete .git folder

--- 
## 📦 Tracking a Project in Git
I track my project and get it ready to push in my GitHub repository
```bash
git status
```
> To check the changes tracked,modified,staged and untracked files.

```bash
git init
```
> Initializes a new git repository.

```bash
git add -A 
```
> Stages all changes including deleted files.

```bash
git add .
```
> Stages all changes in the current working directory.

```bash
git commit -m "<Commit Message>"
```
> Commit the changes from staging area to the git repository.

--- 

## 🌐 Cloning a Remote Git Repository
I clone repositories and enhance them or find issues

```bash
git clone <Link> 
```
> Clones a remote git repository.

```bash
git clone <Link> <name>
```
> Clones a remote git repository to a desired name.

--- 

## 🚫 .gitignore and .gitkeep
Ignoring a git folder / file 

```bash
touch .gitignore
```
> Creates a .gitignore file where other files and folders can be ignored and not tracked.


**Note**
> A .gitignore file can also ignore a file inside a folder.

> Git does not track empty directories. If a directory contains only ignored files, Git will ignore the entire directory.

**Wildcards in .gitignore**
> .gitignore supports pattern matching, so you don't have to list every file individually.
 
```
*.log
```
> Ignores every file ending in `.log`, no matter where it is in the project.
 
```
*.txt
!important.txt
```
> Ignores all `.txt` files, except `important.txt` — the `!` un-ignores a specific match.
 
```
build/
```
> Ignores an entire folder named `build`, wherever it appears.
 
```
/dist
```
> The leading `/` restricts this to only the `dist` folder at the project root, not any `dist` folder nested deeper in the project.
 
```
temp?.txt
```
> The `?` matches exactly one character — this ignores `temp1.txt`, `tempA.txt`, but not `temp10.txt`.

```bash
touch .gitkeep
```
> A .gitkeep file is used to keep an otherwise empty directory tracked by Git.

> Used to track Empty Directories.

--- 
## 🔍 Changes between Commits and Staging Area
After Staging,Modifying the repository will show it as `not staged` although git `status` is used to compare
```bash
git diff
```
> It compares current working directory and staging area.

```bash
git diff --staged
```
> Compares the previous commit and staged area.

> For example:
```diff
-Hello guys(removed)
+Hello guys i am Ayaan(Added)
```
---
## ⚡ Skipping Staging Area
To skip staging area and directly commit

```bash
git commit -a -m "<Direct Commit>"
```
> It adds and commits directly.

> Untracked files(new files/folders that haven't been staged) are not committed

> Does not add new files.

---
## 🔀 Moving and Renaming Files
Untracking a file by moving it or deleting it and Renaming the file without changing to the Desktop 

```bash
git rm --cached <File name>
```
> Untracks the File.

> Add the file in .gitignore and untracking it,since git has internally tracked the file or folder before.

```bash
git mv <old File name> <Current File name>
```
> Renames the file and also stages it.

> Can be Checked through `git status`.

---

## 📜 View and Change Commits
Viewing at the history of commits and changing user-defined commit messages

```bash
git log -p
```
> Shows the differences of each commit as history.
```bash
git log -p <number>
```
> Shows recent commit up till specified number.

```bash
git log --stat
```
> Shows changes in a brief manner, including insertions and deletions.

```bash
git log --pretty=oneline
```
> Displays each commit on a single line.

```bash
git log --pretty=short
```
> Displays a short commit log, including author and commit message.

```bash
git log --pretty=full
```
> Displays full author and commit message.

```bash
git log --since="2026-05-01" (or) git log --since="2 days ago"
```
> Shows commits made with in specified duration.

```bash
git log --pretty=format:"%h -- %an"
```
> Shows hash and Author name in a log.

**NOTE**
> These options of format can be different and can be learned from documentation itself i.e,
https://git-scm.com/docs/pretty-formats.

```bash
git commit --amend
```
> Used to modify the most recent commit message or include more changes in the last commit.

---

## ↩️ Unstaging and Unmodifying/Restoring

```bash
git restore --staged <filename>
```
> To unstage a staged file/folder.

```bash 
git checkout -- <filename>
```
> Revert the changes of the file/folder into previous working committed state.

```bash
git checkout -f
```
> Reverts all the changes into previous working committed state.

> ⚠️ Be careful before using this command. It permanently discards your local changes.

---

## 🌐 Working With Remote Repository

```bash
git remote add origin git@github.com:<GitHub-Username>/<repository-name>.git
```
> Adds a remote repository named `origin` to your local Git repository.

```bash
git remote
```
> Lists all the remote repositories associated with the current Git repository.

```bash
git push -u origin master
```
> Pushes the committed changes to the `master` branch of the remote repository and sets it as the default upstream branch.

> ⚠️ If your default branch is `main`, use:

```bash
git push -u origin main
```

> 🔐 For private repositories, authentication is required.

> We use SSH keys (or a Personal Access Token when using HTTPS) to authenticate with GitHub.

**📚 Refer to the GitHub documentation for setting up SSH keys.**

---






