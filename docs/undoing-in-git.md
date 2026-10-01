<!-- prettier-ignore-start -->
# Undoing In Git
{: .no_toc }

Undoing changes is one of the biggest advantages of using version control. Git has a multiple ways to undo.

## Table of Contents
{: .no_toc }

1. TOC
{:toc}

<!-- prettier-ignore-end -->

## The Ways to Undo

There are 4 main ways to undo changes in Git:
 - Checkout (Slightly dangerous)
 - Reset (Destructive)
 - Revert (Safe)
 - Clean (Slightly dangerous)

## Checkout

The checkout command discards uncommited local changes.

#### When to use it

Use the checkout command if:
 - You regret your uncommitted change(s) and want to undo it.

**WARNING:** The discarded changes cannot be recovered! Be sure of your decision!

#### The Command

`git checkout .`
If you want to revert all folders and files to the most recent commit.

`git checkout file.fe`
If you want to revert a specific file to the most recent commit.

## Reset

The reset command undos one or more commits in the local repository.

There are two common types of reset:
 - Hard reset
 - Soft reset

#### Hard Reset

`git reset --hard [commit id]`
Changes your working directory to match a specific commit.

**WARNING:** Uncommitted changes lost. All files are reset to the specified commit

#### Soft Reset

`git reset --soft [commit id]`
Keeps your changes in the working directory, but still resets the HEAD.

**WARNING:** HEAD and your working directory may differ if you had uncommited changes.

## Revert

The revert command is used to run a specific commit in reverse. Typically, it is used to undo a commit that has been shared with others.

#### The Command

`git revert <commit id>`
Creates a new commit that undoes changes from the specified commit.

##### Multiple Reverts

There are a few ways to revert multiple commits.

```
 git revert Commit1
 git revert Commit2
```
You can run the command mutiple times to revert multiple commits.

`git revert Commit1^..Commit2`
You can revert a sequence of commits. Each commit is reverted separately. 

```
 git revert -n Commit1^..Commit2
 git commit -m "Revert commits 1 through 2 inclusively."
```
If you only want a single revert commit, use the `-n` (stands for "no commit"). Then, commit your changes afterwards.

## Clean

The clean command removes untracked files in a repository's working directory.

To clarify, **untracked files** are files created inside the working directory but have not been added using the `git add .` command. 

#### The Command

`git clean -n`
This command shows all files that will be deleted when you execute the clean command.

```
 git clean -f
 git clean --force
```
This command deletes all untracked files in the repository. 

`git clean -f <path>`
You can also delete specific untracked files. 

## Choosing the right Undo

Here is a general guide on how to choose the correct undo method for your situation:
 - If you want to remove untracked files, use `git clean`.
 - If you want to undo uncommitted changes, use `git checkout`.
 - If you want to undo committed changes:
    - Use `git revert` if you want to be non-destructive.
    - Use `git reset` if you want to be destructive.
 - If you want to undo pushed changes, use `git revert`.