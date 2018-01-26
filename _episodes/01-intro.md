---
layout: episode
title: Introduction and motivation
teaching: 15
exercises: 0
questions:
  - What is version control and why?
  - What are commits and branches?
  - What is a repository?
  - What is Git?
  - What is GitHub?
objectives:
  - Get a mental representation for commits and branches.
  - Motivate why Git and GitHub are so popular.
  - Understand the difference between Git and GitHub.
---

## Goal of this tutorial

- Get a grasp of Git and GitHub without the command line


### What we will not cover

- Command line
- Configuring Git
- Cloning, pushing, pulling
- Rebasing and squashing
- HEAD pointer
- Git under the hood
- Tags

---

## What are version control tools?

- Version control is a tool that can record snapshots of a project.
- You can picture version control like regularly taking a photo of your work.

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

## Git

- Git is a tool that can record and synchronize snapshots.
- Git is not the only tool that can record snapshots (other popular tools are Subversion and Mercurial).

---

## GitHub

- GitHub is a service that provides hosting for Git repositories with a nice web interface.
- GitHub is not the only service that provides this (other popular services are GitLab and Bitbucket).

---

## Commits are snapshots

- A commit is a snapshot of the project (like regularly taking a photo of your work).

Four snapshots on one branch (c1 is the oldest, c4 the most recent snapshot):

![]({{ site.baseurl }}/img/four-snapshots.svg)

---

## Branches

- Commits form a graph (directed and acyclic).
- The graph can branch (c2) and merge (m1).
- Git branches are pointers (labels) to commits.
- Often we call the main development line `master`.

Here we have two branches, one is called `master`, the other is called `some-idea`:

![]({{ site.baseurl }}/img/two-branches.svg)

When we talk about a branch, we often mean the commit with the particular "label" and
all its parent commits since the beginning of the project.

---

## Repositories

- The whole thing (all commits and branches) are a repository.
- We can store the repository in one or several places
 (GitHub, GitLab, Bitbucket, laptop, desktop, cloud, USB key, ...).

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

## How do these concepts look in real life?

- Example: [commits on GitHub](https://github.com/neicnordic/ahm18.neic.nordforsk.org/commits/master).
- Example: [branches on GitHub](https://github.com/neicnordic/ahm18.neic.nordforsk.org/network).
- Example: [commit annotation on GitHub](https://github.com/neicnordic/ahm18.neic.nordforsk.org/commit/2b9c551d41529fb1372dc281b7384c842899834c).
- Commits are uniquely labeled by their checksum.
