---
layout: episode
title: Collaborating on a project using forks
teaching: 10
exercises: 30
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

For **all other situations** it is **always** advisable to first create a new branch on the fork
before doing any modification and to regard upstream branches as read-only. In other words: always
submit a pull requests from a new branch, never from the branch that you wish to modify, except if you
wish to preview changes on `gh-pages` branch.

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

It contains one branch and the branch is called `gh-pages`.

Central repo:
![]({{ site.baseurl }}/img/forking-c-01.svg)


### 2) We fork (copy) the repository

Here two persons create two forks in total but we could imagine creating many forks.
Some software projects have thousands of forks!

<table>
  <tr>
    <td>
      Central repo
    </td>
     
    <td>
      Fork X
    </td>
      
    <td>
      Fork Z
    </td>
  </tr>
  <tr>
    <td>
      <img src="{{ site.baseurl }}/img/forking-c-01.svg"/>
    </td>
     
    <td>
      <img src="{{ site.baseurl }}/img/forking-c-01.svg"/>
    </td>
      
    <td>
      <img src="{{ site.baseurl }}/img/forking-c-01.svg"/>
    </td>
  </tr>
</table>


### 3) Now both persons commit changes

Test whether you can see your changes on your forked website (**NEED EXAMPLE/SCREENSHOT**)

<table>
  <tr>
    <td>
      Central repo
    </td>
     
    <td>
      Fork X
    </td>
      
    <td>
      Fork Z
    </td>
  </tr>
  <tr>
    <td>
      <img src="{{ site.baseurl }}/img/forking-c-01.svg"/>
    </td>
     
    <td>
      <img src="{{ site.baseurl }}/img/forking-x-01.svg"/>
    </td>
      
    <td>
      <img src="{{ site.baseurl }}/img/forking-z-01.svg"/>
    </td>
  </tr>
</table>


### 4) Once we are done, submit pull request towards master on central repo

Here we need a screenshot.


### 5) Accept pull requests

We may decide to first merge the pull request from person X. After merging the pull
request a new merge commit is created, authored by the person accepting the pull request:

<table>
  <tr>
    <td>
      Central repo
    </td>
     
    <td>
      Fork X
    </td>
      
    <td>
      Fork Z
    </td>
  </tr>
  <tr>
    <td>
      <img src="{{ site.baseurl }}/img/forking-c-02.svg"/>
    </td>
     
    <td>
      <img src="{{ site.baseurl }}/img/forking-x-01.svg"/>
    </td>
      
    <td>
      <img src="{{ site.baseurl }}/img/forking-z-01.svg"/>
    </td>
  </tr>
</table>

And then merge the pull request from person Z:

<table>
  <tr>
    <td>
      Central repo
    </td>
     
    <td>
      Fork X
    </td>
      
    <td>
      Fork Z
    </td>
  </tr>
  <tr>
    <td>
      <img src="{{ site.baseurl }}/img/forking-c-03.svg"/>
    </td>
     
    <td>
      <img src="{{ site.baseurl }}/img/forking-x-01.svg"/>
    </td>
      
    <td>
      <img src="{{ site.baseurl }}/img/forking-z-01.svg"/>
    </td>
  </tr>
</table>

Observe:

- Accepted commits are "braided in".
- Nothing happened to the forks: they do not get
  automagically updated once the central repository is changed.


### 6) Update forks

Both forks are outdated. They do not contain changes from the other person(s).

FIXME: here we need screenshots and this is the place where we need to execute 4 commands

```bash
# we clone our fork onto our laptop
git clone https://github.com/fork/example.git

# we step into the newly created directory
cd example

# pull updates from the central repository
git pull https://github.com/central/example.git gh-pages

# push updates to the fork
git push https://github.com/fork/example.git gh-pages
```

Sitaution after we have updated the forks:

<table>
  <tr>
    <td>
      Central repo
    </td>
     
    <td>
      Fork X
    </td>
      
    <td>
      Fork Z
    </td>
  </tr>
  <tr>
    <td>
      <img src="{{ site.baseurl }}/img/forking-c-03.svg"/>
    </td>
     
    <td>
      <img src="{{ site.baseurl }}/img/forking-c-03.svg"/>
    </td>
      
    <td>
      <img src="{{ site.baseurl }}/img/forking-c-03.svg"/>
    </td>
  </tr>
</table>
