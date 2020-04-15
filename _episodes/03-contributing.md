---
layout: episode
title: Contributing to existing repositories
teaching: 10
exercises: 30
questions:
  - How to submit small changes using pull requests
  - How to propose and submit larger changes
  - How to review and discuss changes
objectives:
  - ...
---

## Contributing to existing repositories

In this session we will learn how to contribute to repositories which either
belong to others or belong to a group that you are part of.

We will do this in a progression from a small trivial fix to a change proposal
and discuss the pros and cons.


### Note to instructors

The instructor will prepare an example repository and share the link with the
participants (see instructor guide for more details).

---

### Step 1: Learn how to add collaborators to your repository

Now we know how to share repositories and the first step to allow changes by
others would be to add your group members or collaborators as "collaborators"
under GitHub.

(instructor shows how, later we add screenshots)

From here on everybody can push changes in the same way as we have done in a
single-person repository in the previous episodes.

> ## Discussion
>
> - Discuss the advantages and possible disadvantages of this setup.
{: .discussion}

---

### Step 2: Submit a trivial change via the web interface

We will now assume that either we are not a collaborator of the repository,
or the `master` branch is protected and we cannot push to it directly.

(instructor shows how to protect branches, later we add screenshots)

We will practice this by fixing a typo in an example text.

> ## Discussion
>
> - Protecting the `master` branch "forces" all changes to it to be reviewed first.
    **We recommend this for group repositories**.
    Discuss the advantages of this.
> - What is a conflict in Git?
> - Can you anticipate conflicts?
> - What can we do to avoid conflicts?
{: .discussion}

---

### Step 3: Contributing non-trivial changes

Submit a larger change using GitHub Desktop by first opening an issue.

Optional exercise:
- Sending a pull request with a typo/mistake in it and adjusting the pull request with a subsequent commit
