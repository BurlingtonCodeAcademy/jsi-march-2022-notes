# Session-08

We started off class by reviewing and building upon our knowledge of **scope**. We spent the rest of class learning how to work with Git and GitHub, and finally, an introduction to your first project: "Guess The Number" (due on Thursday, 4/7)

## Scope

Remember: The **Scope** is a context, including all the variables accessible from a given code location. Inner scopes can see out, but outer scopes cannot see in.

## Global Functions

Unless nested within another function, or code-block, functions are global.

## Nested Functions

You can call functions within other functions.
You can also create functions within other functions.

You can nest functions within functions within functions, just **Keep in mind** that the more nested your code is, the more _buggy_ your code can get.

## Git

Git is a distributed version control tool used for tracking changes to files.
Git tracks:

- updates to code
- who made those updates
- when those updates were made

Git is powerful and is a vital tool for any...

- dev team
- individual on that dev team
- product manager or client
- sysadmin
- QA (Quality Assurance) engineer

## Repository & Initializing a Git Repository

A repository (or "repo") contains the version history of a collection of files. In git, a repo comprises all files and subdirectories inside a single "root" directory.

- the command `git init` makes it into a repo
- the command `git status` describes the state of the current repo

[Git Documentation](https://git-scm.com/docs/git)

## Two-Step Process for Tracking Changes

Git has a two-step process for tracking changes to files:

1. `git add .` => adds changes made to your files
2. `git commit -m "some message"` => commit's a message descriptive of changes made

**First,** you add the changes to the staging area (also called the cache or the index)
**Then,** you commit the changes to the history (also called the log)

After a commit, the staging area is cleared, and the cycle continues.

Every commit has a unique id (also known as a hash), which is a long string of letters and numbers. See example below:
```js
commit 
d8b95657eebea7083de1a4fb96ba7fb296637342
```

## Publishing changes to GitHub

- `git push` => pushes committed changes to GitHub

- `git pull` => allows you to incorporate a change someone else has made

## Summary 

- `git init` initializes a repo inside a directory
- `git add .` stages all current local changes, including new files and edits inside existing files
- `git commit -m "message"` turns the staged changes into a new commit history entry
- `git show` expands a single commit to show the metadata and changes
- a git ID is a SHA-1 hash that uniquely identifies a single commit
- `git push` sends your change history to a remote repository
- `git pull` gets new changes from a remote repository

## Reading & Homework

- Complete the **"Guess The Number"** project **due on Thursday, April 7th**
