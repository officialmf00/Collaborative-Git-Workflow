---
layout: default
title: Stashing
nav_order: 7
---
<!-- prettier-ignore-start -->
# Stashing
{: .no_toc }

Stashing is a way to allow you to put aside changes that you don't want to commit immediately.

## Table of Contents
{: .no_toc }

1. TOC
{:toc}

<!-- prettier-ignore-end -->

## When to Stash

Here are some situations where you would want to stash:
 - You want to switch branches, but you're in the middle of something and don't want to commit yet.
 - You need to pull changes, but you have uncommitted work.

## The Basic

`git stash` 
This is the command that stashes your changes, leaving you with a clean working directory.

Think of `git stash` as creating a stack of saved changes. You can stash multiple sets of changes and Git will store them in a LIFO (Last In, First Out) stack.

## Restoring Stashed Changes

`git stash pop`
This command re-applies the changes and removes them from the stash.

`git stash apply`
This command re-applies the changes but keeps them in the stash.

## The Advanced

Now, you know the most essential Stash commands. Here are other useful commands to know!

`git stash list` 
Review all your stashes before deciding to apply or drop them. 

`git stash drop` : 
Removes the most recent stash from the stack without applying it. 

`git stash branch <branchname>`
Creates a new branch based on the popped stash.

`git stash clear` 
Removes all your stashes. 

`git stash pop 'stash@{n}'` 
Pop a specific stash seen in git stash list.
