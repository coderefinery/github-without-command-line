---
layout: episode
title: Collaborating on a project using forks
teaching: 10
exercises: 20
questions:
  - What are forks?
  - How can we collaborate via forks?
  - How can we submit and accept external contributions to projects?
objectives:
  - Get a mental picture of the fork-pull-request workflow.
  - Be able to synchronize changes between repositories.
---

## Exercise

In this exercise we will collaborate on a repository by forking it.
We will improve a simple website together. In this example we will find it advantageous
to not create new branches so that we can preview the modified website on our forked repositories.

For all other situations it is *always* advisable to first create a new branch on the fork
before doing any modification and to regard upstream branches as read-only.

Our plan:

- Fork an example repository, if you already have a fork, update it first (last point)
- Commit a change
- Submit pull request towards the central repository
- Pull requests are reviewed and integrated
- Possible conflicts are discussed and resolved
- Commit graph is reviewed and discussed
- We update all forks

**TODO**: add more text, context, and screenshots, explain briefly what a fork is


### 1) We start out with a relatively simple central repository

Central repo:
![]({{ site.baseurl }}/img/forking-c-01.svg)


### 2) We fork (copy) the repository

Here two persons create two forks in total but we could imagine creating many forks.
Some software projects have thousands of forks!

Central repo:
![]({{ site.baseurl }}/img/forking-c-01.svg)

Fork A:
![]({{ site.baseurl }}/img/forking-c-01.svg)

Fork B:
![]({{ site.baseurl }}/img/forking-c-01.svg)


### 3) Before we do any work, we always first branch

Central repo:
![]({{ site.baseurl }}/img/forking-c-01.svg)

Fork A:
![]({{ site.baseurl }}/img/forking-a-01.svg)

Fork B:
![]({{ site.baseurl }}/img/forking-b-01.svg)


### 3) Now both persons commit changes

Central repo:
![]({{ site.baseurl }}/img/forking-c-01.svg)

Fork A:
![]({{ site.baseurl }}/img/forking-a-02.svg)

Fork B:
![]({{ site.baseurl }}/img/forking-b-02.svg)


### 4) Once we are done, submit pull request towards master on central repo

Here we need a screenshot.


### 5) Accept pull requests

Again we may decide to first merge the pull request from person B:

Central repo:
![]({{ site.baseurl }}/img/forking-c-02.svg)

Fork A:
![]({{ site.baseurl }}/img/forking-a-02.svg)

Fork B:
![]({{ site.baseurl }}/img/forking-b-02.svg)

And then merge the pull request from person A:

Central repo:
![]({{ site.baseurl }}/img/forking-c-03.svg)

Fork A:
![]({{ site.baseurl }}/img/forking-a-02.svg)

Fork B:
![]({{ site.baseurl }}/img/forking-b-02.svg)

**Super important**: notice that nothing happened to the forks. They do not get
automagically updated once the central repository is changed.


### 6) Update forks

Both forks are outdated. They do not contain changes from the other person(s).

FIXME: here we need screenshots and this is the place where we need to execute 4 commands

```bash
git clone https://github.com/fork/example.git
cd example
git pull https://github.com/central/example.git master
git push https://github.com/fork/example.git master
```

Sitaution after we have updated the forks:

Central repo:
![]({{ site.baseurl }}/img/forking-c-03.svg)

Fork A:
![]({{ site.baseurl }}/img/forking-a-03.svg)

Fork B:
![]({{ site.baseurl }}/img/forking-b-03.svg)
