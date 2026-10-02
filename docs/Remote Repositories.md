---
layout: default
title: Remote Repositories
nav_order: 9
---

<!-- prettier-ignore-start -->
# Remote Repositories
{: .no_toc }

A short introductory paragraph for the module to come before the table of contents.

## Table of Contents
{: .no_toc }

1. TOC
{:toc}

<!-- prettier-ignore-end -->

## Remote Repositories

A remote repository is a version of your project that is hosted on a remote server.

Remote repositories can interact with local repositories, allowing you to push your

changes to others and pull their changes to your local repository.

## Adding / Configuring a GitHub Remote

To add a new remote, use the git remote add command on the terminal, in the directory your repository is stored at.

The git remote add command takes two arguments:

    A remote name, for example, origin
    A remote URL, for example, https://github.com/OWNER/REPOSITORY.git

For example:

$ git remote add origin https://github.com/OWNER/REPOSITORY.git
# Set a new remote

$ git remote -v
Verify new remote
> origin  https://github.com/OWNER/REPOSITORY.git (fetch)
> origin  https://github.com/OWNER/REPOSITORY.git (push)


## Pushing and Pulling

Pull
 
- Combines Fetch and Merge.
 
. Downloads the latest commits and automatically merges them into your current branch.

Push
 
- Uploads your latest commits to the remote repo. (If your local branch has diverged from the remote branch, you may need to pull first.)
