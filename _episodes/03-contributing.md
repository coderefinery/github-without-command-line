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

- [Step 1: Learn how to add collaborators to your repository](#step-1-learn-how-to-add-collaborators-to-your-repository)
- [Step 2: Submit a trivial change via the web interface](#step-2-submit-a-trivial-change-via-the-web-interface)
- [Step 3: Resolving a conflict](#step-3-resolving-a-conflict)
- [Step 4: Contributing non-trivial changes](#step-3-contributing-non-trivial-changes)


### Note to instructors

The instructor will prepare an example repository and share the link with the
participants (see instructor guide for more details).

> ## Recap: different methods to "download" a repository
>
> - There is no need to download each file one by one.
> - You can either download the repository as ZIP file (green button "Clone or download") if you do not plan to change files
    and if you are sure that you don't need to browse the history of file changes.
> - **Possibly better: you clone the repository** (green button on the web or through GitHub Desktop or using command line) so that you
    can apply and track changes and possibly share them later.
> - Cloning copies not only the latest version but all snapshots and all branches and tags: entire history.
{: .discussion}

---

### Step 1: Learn how to add collaborators to your repository

Now we know how to share repositories and the first step to allow changes by
others would be to add your group members or collaborators as "collaborators"
under GitHub.

- Click on "Settings" (top right), then "Manage access" (left), then "Invite a collaborator" (green button)
- You can try this with one of the repositories which we created in the earlier episodes

<img src="{{ site.baseurl }}/img/contributing/invite-collaborators.png" width="600px" style="border:2px solid #000000;">

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

### Step 3: Resolving a conflict

To be written ...

---

### Step 4: Contributing non-trivial changes

Submit a larger change using GitHub Desktop.  As an example our task will be to
add a new file (in our case taco recipe) to the exercise repository.

- We first open an issue and describe our idea. In the issue we can collect feedback.
- We clone the exercise repository using GitHub Desktop.
- Add the new file to the local repository.
- Create a new branch.
- Try to publish that branch (you may not have write permissions to the repository on GitHub).
- If you don't have write permissions: "Fork this repository", then try to publish the branch to the fork.
- "Create Pull Request"

(instructor shows how, later we add screenshots)

Optional exercise:
- Send a pull request with a typo/mistake in it and adjust the pull request with a subsequent commit. Discuss
  how adjusting pull requests can be a useful mechanism.

---

> ## Summary
>
> - In this episode we learned how to propose changes and submit changes via "pull requests".
> - Protecting the `master` branch and insisting on every change going
>   through a pull request can be useful to get feedback on your changes
>   and to improve knowledge transfer.
> - For controversial changes it can
>   be useful to first discuss in an issue before submitting the changes.
> - Note that you can mark pull requests as draft to collect feedback on unfinished work.
> - Now that you know how to send improvements, we welcome improvements to this material also.
{: .discussion}
