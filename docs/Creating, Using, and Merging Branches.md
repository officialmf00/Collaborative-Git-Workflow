---
layout: default
title: Creating, Using, and Merging Branches
nav_order: 5
---

## Creating, Using, and Merging Branches

### Creating Branches

Creating a new branch:

git branch <branch-name>

Switching to a branch:

git checkout <branch-name>

Create and switch in a single command:

git checkout -b <branch-name>

### Merging Branches

Branching allows for isolated development, and merging brings those developments back into the main timeline.

Let's say we've been working and committing to an experimental branch and we want to merge those commits back into main:

git checkout main
git merge experimental
