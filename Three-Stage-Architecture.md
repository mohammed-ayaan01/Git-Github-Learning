# Three Stage Architecture of Git

Git manages your project through **three areas**. Every file you work with moves through these stages as you `stage` and `commit`.

```
Working Directory       Staging Area          Git Repository
   (your files)         (the "index")         (.git history)
   |                        |                       |
   |   <----------Checkout Project-----------       |
   |                        |                       |
   |    --Add Files->       |   --Commit Files->    |

```

## 1. Working Directory

--> This is your actual project folder — the files you see and edit in VS Code (or any editor).
--> Changes here are **untracked/unstaged** until you tell Git about them.
--> Check what's changed here anytime:
```
git status
```

## 2. Staging Area (a.k.a. "Index")

--> A holding area between your working directory and the repository as files to commit (Intermediate Process).
--> Think of it as a "draft" of your next commit — you choose exactly what goes in.
--> Move changes here with:
```
git add filename.txt
git add .          # stage everything
```
--> You can stage **some** changes and leave others out — this is what makes commits precise instead of "commit everything I touched."

## 3. Git Repository (.git folder)

--> The permanent, saved history of your project.
--> A commit takes a **snapshot** of whatever is currently in the staging area.
--> Move staged changes here with:
```
git commit -m "Describe what changed"
```
--> Once committed, this becomes part of your project's permanent timeline — visible with:
```
git log
```

## Quick Summary

```
1. Edit a file            -->  Working Directory
2. git add filename        -->  Staging Area
3. git commit -m "message" -->  Repository
```

## Why do we need Staging Area??

This trips up a lot of beginners coming from other tools. A couple of reasons it exists:

--> **Precision:** You can commit only *part* of your changes, not everything you've touched. Example: you fixed a bug AND experimented with a new feature in the same session — stage and commit just the bug fix first.

--> **Review before committing:** `git diff` shows unstaged changes, `git diff --staged` shows exactly what's about to be committed — a safety check before it becomes permanent history.

--> **Partial staging:** You can even stage *part* of a single file's changes:
```
git add -p filename.txt
```
This walks you through each change in the file and asks whether to stage it — useful for splitting one messy editing session into clean, logical commits.

## Git File Status and Life Cycle

```
$ git status
$ git init --> Untracked
$ git add . --> Tracking and Unmodified
```

Modifying The File --> Modified

```
$ git add . --> Staged
```

## Key concepts I want to remember

> - Nothing is "saved" in Git history until it's **committed** — staging alone doesn't protect your work permanently.
> - `git add` doesn't mean "save" — it means "mark this for my next commit."
> - You can go back and forth between working directory and staging area as many times as you want before committing.