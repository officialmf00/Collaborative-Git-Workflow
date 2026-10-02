---
layout: default
title: The Git Life Cycle
nav_order: 2
---

<!-- prettier-ignore-start -->
# The Git Life Cycle
{: .no_toc }

A short introductory paragraph for the module to come before the table of contents.

## Table of Contents
{: .no_toc }

1. TOC
{:toc}

<!-- prettier-ignore-end -->

## Untracked Files:
- Files that are created, but git doesn't know about them yet
- The first stage of every file

## Unmodified Files:
- Files that have been pushed to git, but have no edits made to them based on the last push

## Modified Files:
- Files that have edits made to them since the last push

## Staged Files:
- Files that have been staged to be committed to git, but haven't been pushed yet

## The Life Cycle Order
The life cycle goes like this:
**Untracked -> Staged -> Unmodified -> Modified -> Staged**
