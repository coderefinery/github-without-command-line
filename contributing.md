---
layout: episode
title: Contributing to existing repositories
teaching: 20
exercises: 40
questions:
  - How to submit small changes using pull requests
  - How to propose and submit larger changes
  - How to review and discuss changes
---

# Contributing to existing repositories

In this session we will learn how to contribute to repositories which either
belong to others or belong to a group that you are part of.

We will do this in a progression from a small trivial fix to a change proposal
and discuss the pros and cons.


## Note to instructors

The instructor will prepare an example repository and share the link with the
participants (see instructor guide for more details).

> ## Recap: different methods to "download" a repository
>
> - There is no need to download each file one by one.
> - You can either download the repository as ZIP file (green button "Clone or download") if you do not plan to change files
>   and if you are sure that you don't need to browse the history of file changes.
> - **Possibly better: you clone the repository** (green button on the web or through GitHub Desktop or using command line) so that you
>   can apply and track changes and possibly share them later.
> - Cloning copies not only the latest version but all snapshots and all branches and tags: entire history.
{: .discussion}

---

## Step 1: Learn how to add collaborators to your repository

Now we know how to share repositories and the first step to allow changes by
others would be to add your group members or collaborators as "collaborators"
under GitHub.  This allows them to change things directly (but we'll
actually do it with review).

- Click on "Settings" (top right), then "Manage access" (left), then "Invite a collaborator" (green button)
- You can try this with one of the repositories which we created in the earlier episodes

<img src="{{ site.baseurl }}/img/contributing/invite-collaborators.png" width="800px" style="border:2px solid #000000;">

From here on the collaborators can push changes in the same way as we have done in a
single-person repository in the previous episodes.

> ## Discussion
>
> - Discuss the advantages and possible disadvantages of this setup.
{: .discussion}

---

## Step 2: Submit a small change via the web interface as collaborator

In the last episodes we learned how to directly commit changes either via web
or via the desktop and you need to be a collaborator (have write permissions)
to be able to do that.

In this exercise we will not change the `master` branch directly but
we will submit a "pull request" (a **change proposal**) towards the `master` branch
for **code review**.

**Exercise**: We will practice this by fixing a typo in an example text.

- Instructor shares an example repository and adds a volunteer learner as collaborator
- Learner shares screen and edits an example file via web (click on the edit pen)
- We find a typo and correct it
- We do not commit directly to `master` but rather "Create a new branch for this commit and start a pull request."
- We choose a meaningful branch name (it can be useful to prefix it with your name so that we know who this branch belongs to)

<img src="{{ site.baseurl }}/img/contributing/propose-file-change.png" width="800px" style="border:2px solid #000000;">

- After we click "Propose file change" we are taken to this form:
<img src="{{ site.baseurl }}/img/contributing/pull-request-form.png" width="400px" style="border:2px solid #000000;">

- In there we verify the **source and target branch**, verify the **file changes**,
  can edit the **title** and **description** of the "pull request" (change proposal)
- After we have submitted the "pull request", one of our collaborators can review it
- We can discuss and ask for changes before merging the changes "Merge pull request"

> ## Discussion
>
> - Ideally submitter and reviewer should be two different persons.
>   When is this best? When not?
> - You can modify an open "pull request" by committing new changes to the branch
> - Review is not only to assure quality but also to enhance learning and **knowledge transfer** within the group
{: .discussion}

---

To make sure that *all* changes of the `master` branch are reviewed and nobody
can push commits to it directly, it can be useful to "protect" branches.

- "Settings", then "Branches", then "Add rule":

<img src="{{ site.baseurl }}/img/contributing/branch-protection.png" width="800px" style="border:2px solid #000000;">

> ## Discussion
>
> - Protecting the `master` branch "forces" all changes to it to be reviewed first.
    **We recommend this for group repositories**.
    Discuss the advantages/disadvantages of this.
{: .discussion}

---

## Step 3: Submit a small change via the web interface as external contributor

Submitting a change proposal as external contributor (we assume you are not added
as "collaborator" and thus have no write-permissions to a repository) looks very similar
to submitting a "pull request" to a repository with a protected `master` branch.
Only this time you have no other choice than "Propose file change".

Let's try this with one participant who has not been added as collaborator
sharing screen:
- Edit a file with the "pen" button
- Edit the commit message and click green button "Propose file change"
- This creates a **fork** of the repository (GitHub makes a copy of the original repository to your user space)
- You can now still review the change before submitting it, green button "Create pull request"
- Later you can remove the fork if you like

---

## Step 4: Resolving a conflict

### Note to instructors

- "Non-talking instructor" prepares a conflicting commit during session (check
  what the first PR does).
- Conflict can be shown as demo.


### Exercise/demo: let us experience a conflict

**When merging** two branches a conflict can arise when the same file **portion**
has been modified in two **different** ways on the two branches.

We can practice how a conflict looks and how to resolve it:
- Two participants should send two "pull requests" (change proposals)
  branching from `master` changing the same line in two different ways

<img src="{{ site.baseurl }}/img/contributing/conflict-edit-1.png" width="400px" style="border:2px solid #000000;">
<img src="{{ site.baseurl }}/img/contributing/conflict-edit-2.png" width="400px" style="border:2px solid #000000;">

- We merge together one of the pull requests (this will work)
- Then we try to merge the other and we see a conflict:

<img src="{{ site.baseurl }}/img/contributing/conflict-pull-request.png" width="600px" style="border:2px solid #000000;">

- We try to resolve the conflict via web
- Choose the version that you wish to keep, remove conflict markers, "Mark as resolved" and commit the change

<img src="{{ site.baseurl }}/img/contributing/conflict-resolution.png" width="800px" style="border:2px solid #000000;">

> ## Discussion
>
> - Compare with Google Docs: can you get conflicts there? What are the advantages and disadvantages?
> - What can we do to avoid conflicts?
{: .discussion}

---

## Step 5: Contributing non-trivial changes

Submit a larger change using GitHub Desktop.  As an example our task will be to
add a new file (in our case a taco recipe) to the exercise repository.


### Note to instructors

- A participant shares screen and creates a repository, then instructor takes screen share and
  we go through steps to contribute to that repository (without write permissions), then
  screen share goes back to participant and we together review this change


### Exercise

- We first open an issue via the web interface
  and describe our idea. In the issue we can collect feedback
- We clone the exercise repository using GitHub Desktop
- Create a new branch
- Add the new file to the local repository
- Commit and refer to the issue (e.g. here closing issue number 12: "this is the commit message, closes #12")
- Try to publish that branch (you may not have write permissions to the repository on GitHub)
- If you don't have write permissions: "Fork this repository", then try to publish the branch to the fork
- "Create Pull Request"
- If you forgot to refer to the issue in the commit, you can [refer to the issue](https://help.github.com/en/github/managing-your-work-on-github/linking-a-pull-request-to-an-issue) in the pull request


### Bonus exercise

- Send a pull request with a typo/mistake in it and adjust the pull request with a subsequent commit. Discuss
  how adjusting pull requests can be a useful mechanism.

---

> ## Summary
>
> - In this episode we learned how to propose changes and submit changes via "pull requests".
> - If you track and collaborate on text files it can be useful to wrap lines. If the entire
>   paragraph is one long line, if will be more difficult to see what changed,
>   and you risk seeing more conflicts.
> - Protecting the `master` branch and insisting on every change going
>   through a pull request can be useful to get feedback on your changes
>   and to improve knowledge transfer.
> - For controversial changes it can
>   be useful to first discuss in an issue before submitting the changes.
> - Note that you can mark pull requests as draft to collect feedback on unfinished work.
> - Now that you know how to send improvements, we welcome
>   improvements to [this material](https://github.com/coderefinery/github-without-command-line) also.
{: .discussion}
