<!-- prettier-ignore-start -->
# Tags
{: .no_toc }

Tags in Git are like bookmarks for important events or milestones in your project. They're often used to mark release points (v1.0.0, v1.1.0, etc.).

## Table of Contents
{: .no_toc }

1. TOC
{:toc}

<!-- prettier-ignore-end -->

## Tag Naming

Before diving into the commands, there are some naming conventions to follow when creating tags.
 - Tag names should not include spaces. 
 - They should only include characters (a-z), (A-Z), numbers (0-9) and the dash/hyphen (-).

## Creating lightweight tags

```
 git tag <tag-name>
 git tag <tag-name> <commit hash>`
```

This command will tag the current or specified commit with the provided tag name.

## Creating annotated tags

`git tag -a <tag-name> -m "Additional metadata goes here"`
This command will tag the current commit with the provided tag name. This tag also store additional metadata such as the tagger's name, email, date, and an optional message.

`git show <tag-name>`
This command shows you the associated information with the provided tag name.

## Tag Abilities

Here are additional commands that will help you use tags to their fullest potential.

#### Checkout

`git checkout <tag-name>`
You can treat the tag like a branch/commit, and checkout to the tag's point in history.

#### Lists

```
 git tag
 git tag -l
```
You can list all the tags in the repository.

To narrow the list based on a search pattern, you can use `git tag -l "<search-pattern>"`.

#### Differences

`git diff <tag-name>`
You can compare the differences between the tagged state of the code and the current HEAD.
