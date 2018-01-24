---
layout: episode
title: Collaborating on a project within the same repository
teaching: 5
exercises: 20
questions:
  - How can teams collaborate within the same repository?
objectives:
  - Learn how to submit, review, and accept pull requests.
---

## Exercise

Goal of the exercise: collaboratively improve a recipe together. Ideally a recipe
with several files to minimize chance of conflicts.

- Start from a repo that contains a recipe
- Add participants as collaborators
- Distribute tasks
- Each participant creates a branch and implements changes
- Submit pull request
- Pull requests are reviewed and integrated
- Possible conflicts are discussed and resolved
- Commit graph is reviewed and discussed

TODO: add more text, context, and screenshots

We will start with one `master` branch containing two commits:

![]({{ site.baseurl }}/img/collaborative-01.svg)

Before we do any work, each of the participants creates own branch:

![]({{ site.baseurl }}/img/collaborative-02.svg)

We can imagine that person A records two commits on branch `person-a/feature`
(use a meaningful branch name):

![]({{ site.baseurl }}/img/collaborative-03.svg)

Person B might record one commit on branch `person-b/feature`:

![]({{ site.baseurl }}/img/collaborative-04.svg)

Now all participants submit a pull request towards the `master` branch.

We may decide to merge the pull request from person B first:

![]({{ site.baseurl }}/img/collaborative-05.svg)

Then we may merge the pull request from person A:

![]({{ site.baseurl }}/img/collaborative-06.svg)

Branches `person-b/feature` and `person-b/feature` might still be there depending on whether
we asked them to be removed after the pull request is accepted.
If they are still there, we wish to remove them now:

![]({{ site.baseurl }}/img/collaborative-07.svg)

Notice that we have not removed any snapshots.
