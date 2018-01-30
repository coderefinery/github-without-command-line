---
layout: episode
title: Collaborating using the same repository
teaching: 5
exercises: 30
questions:
  - How can teams collaborate within the same repository?
objectives:
  - Learn how to submit, review, and accept pull requests.
---

## Exercise

**Goal**

- Collaboratively improve a [recipe](https://github.com/coderefinery/exercise-collaborative-recipe) together.
- The [example repository](https://github.com/coderefinery/exercise-collaborative-recipe)
  contains several files to minimize chance of conflicts.

**Before we start**

- Participants work in groups of two
- The instructor adds one user of each group as collaborator to the repository
- Each group will edit one file

**This is what participants will do**

- Each group creates a branch and implements changes
- Submit pull request
- Pull requests are reviewed and integrated
- Possible conflicts are discussed and resolved
- Commit graph is reviewed and discussed


### 1) Beginning

We will start with one `master` branch containing two commits:

![]({{ site.baseurl }}/img/collaborative-01.svg)


### 2) Before we do anything, we branch

Before we do any work, each group
[creates own branch](https://help.github.com/articles/creating-and-deleting-branches-within-your-repository/).

Here we for simplicity only show two new branches:

![]({{ site.baseurl }}/img/collaborative-02.svg)


### 3) Commit to the branch

We can imagine that one group records two commits on branch `soup`:

![]({{ site.baseurl }}/img/collaborative-03.svg)

Another group might record one commit on branch `appetizer`:

![]({{ site.baseurl }}/img/collaborative-04.svg)


### 4) Submit pull request

Once you are done with your changes,
[submit a pull request](https://help.github.com/articles/creating-a-pull-request/#creating-the-pull-request)
towards the `master` branch.

Pull request means: "here are my changes, please review them and possibly merge them"


### 5) Merge pull requests

**You can stop here, we do this part together on the big screen.**

We may decide to merge the work on the appetizer first:

![]({{ site.baseurl }}/img/collaborative-05.svg)

Then we may merge the work on the soup course:

![]({{ site.baseurl }}/img/collaborative-06.svg)


### 6) Possibly clean up merged branches

Branches `soup` and `appetizer` might still be there depending on whether
we asked them to be removed after the pull request is accepted.

If they are still there, we wish to
[delete them](https://help.github.com/articles/creating-and-deleting-branches-within-your-repository/#deleting-a-branch) now:

![]({{ site.baseurl }}/img/collaborative-07.svg)

Notice that we have not removed any snapshots.
