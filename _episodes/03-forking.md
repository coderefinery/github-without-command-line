---
layout: episode
title: Collaborating using forks
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

In this exercise we will collaborate on an
[example repository](https://github.com/coderefinery/exercise-gh-pages) by forking it.
We will improve a
[simple website](https://coderefinery.github.io/exercise-gh-pages/) together.
In this example we will find it advantageous
to not create new branches so that we can preview the modified website on our forked repositories.

For **all other situations** it is **always** advisable to first create a new branch on the fork
before doing any modification and to regard upstream branches as read-only. In other words: always
submit a pull requests from a new branch, never from the branch that you wish to modify, except if you
wish to preview changes on `gh-pages` branch.

**Our plan**

- Work in groups of two
- Fork an example repository, if you already have a fork, update it first (last point)
- Commit one or several changes (each group modifies a specific section in `index.md`)
- Submit pull request towards the central repository
- Pull requests are reviewed and integrated
- Possible conflicts are discussed and resolved
- Commit graph is reviewed and discussed
- We update all forks


### 1) We start out with a relatively simple central repository

It contains one branch and the branch is called `gh-pages`.

Central repo:
![]({{ site.baseurl }}/img/forking-c-01.svg)


### 2) [We fork](https://help.github.com/articles/fork-a-repo/) (copy) the [repository](https://github.com/coderefinery/exercise-gh-pages)

Here two groups create two forks in total but we could imagine creating many forks.

A fork is a full copy.
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


### 3) Now groups commit changes

After you have committed your change(s),
test whether you can see your changes on your forked website: https://**REPLACETHIS**.github.io/exercise-gh-pages/ (replace by
your GitHub username). This website is automatically generated since this project contains a `gh-pages` branch.

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

This is similar to previous exercise with one difference: instead of submitting a pull request
within a repository, we submit it from one repository, to another repository.

See also [this documentation](https://help.github.com/articles/creating-a-pull-request/#creating-the-pull-request).


### 5) Accept pull requests

**You can stop here, we do this part together on the big screen.**

We may decide to first merge the pull request from group X. After merging the pull
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

And then merge the pull request from group Z:

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
  automagically updated once the central repository is changed - verify this by visiting your fork on GitHub.


### 6) Update forks

Both forks are outdated. They do not contain changes from the other groups.

Linux and Mac users: open the terminal. Windows users, start the Git shell (we wait until
everybody is on the same page).

```bash
# we clone our fork onto our laptop
git clone https://github.com/REPLACETHIS/exercise-gh-pages.git

# we step into the newly created directory
cd exercise-gh-pages

# pull updates from the central repository
git pull https://github.com/coderefinery/exercise-gh-pages.git gh-pages

# push updates to the fork
git push https://github.com/REPLACETHIS/exercise-gh-pages.git gh-pages
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

Verify this by visiting your fork on GitHub.

---

## Why forking?

- You do not need write-permissions to the repository: anybody can submit pull requests.
- Keeps the central repository tidy.
