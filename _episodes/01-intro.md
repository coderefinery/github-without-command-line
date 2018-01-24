---
layout: episode
title: Introduction and motivation
teaching: 15
exercises: 0
questions:
  - What is a commit?
  - What is a branch?
  - What is a repository?
  - What is Git?
  - What is GitHub?
objectives:
  - Get a mental representation for commits and branches.
  - Motivate why Git and GitHub are so popular.
  - Understand the difference between Git and GitHub.
---

## Goal of this tutorial

- Get a grasp of Git and GitHub without command line


### What we will not cover

- Command line
- Configuring Git
- Cloning, pushing, pulling
- Rebasing and squashing
- Git under the hood

---

## Commits are snapshots

- A commit is a snapshot of the project (like regularly taking a photo of your work).

Four snapshots on one branch (c1 is the oldest, c4 the most recent snapshot):

![]({{ site.baseurl }}/img/four-snapshots.svg)

---

## What we typically like to snapshot

- Software
- Scripts
- Documents
- Manuscripts
- Configuration files
- Website sources
- Data

---

## Why are snapshots valuable?

- If we discover a problem, we can find out when it was introduced (remember http://heartbleed.com?).
- We have the means to refer to a well-defined version of a project.
- Reproducibility.
- We can often find out why something was introduced.

---

## Branches

- Commits form a graph (directed and acyclic).
- The graph can branch (c2) and merge (m1).
- Git branches and tags are pointers (labels) to commits.
- Often we call the main development line `master`.

Here we have two branches, one is called `master`, the other is called `some-idea`:

![]({{ site.baseurl }}/img/two-branches.svg)

---

## Tags

- Tags are like branches: they point to specific commits.
- Typically they are used to mark a milestone of a project.
- While branch pointers can move when new snapshots are added, tags never move.

---

## Repositories

- The whole thing (all commits, branches, and tags) are a repository.
- We can store the repository in one or several places (GitHub, GitLab, Bitbucket, laptop, desktop, cloud, where-ever we like).

---

## Why using repositories

- All changes are recorded.
- We do not have to send changes via email.
- We can experiment with several ideas which might not work out (using branches).
- Several people can work on the same project at the same time (using branches).
- We do not have to wait for others to send us "the latest version" over email.
- We do not have to merge parallel developments by hand.
- It is possible to serve websites directly from a repository.

---

## Git

- Git is a tool that can record commits and allows us to branch and merge and much more.
- Git is not the only tool that can record snapshots (other popular tools are Subversion and Mercurial).

---

## GitHub

- GitHub is a service that provides hosting for Git repositories with a nice web interface.
- GitHub is not the only service that provides this (other popular services are GitLab and Bitbucket).

---

## FIXME

- look at commits on github
- look at branches on github
- look at commit annotation (commit message, date, author, hash)
- explain why commits have hashes and are not simply numbered
