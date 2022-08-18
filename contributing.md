# Contributing to existing repositories using pull requests

In this session we will learn how to contribute to repositories which either
belong to a group that you are part of or
belong to others.

We will do this in a progression from a small trivial fix to a change proposal
and discuss the pros and cons.

> ## Recap: different methods to "download" a repository
>
> - There is no need to download each file one by one.
> - You can either download the repository as ZIP file (green button "Clone or download") if you do not plan to change files
>   and if you are sure that you don't need to browse the history of file changes.
> - **Possibly better: you clone the repository** (green button on the web or through GitHub Desktop or using command line) so that you
>   can apply and track changes and possibly share them later.
> - Cloning copies not only the latest version but all snapshots and all branches and tags: entire history.
{: .discussion}

```{instructor-note}
- The instructor will prepare an example repository and share the link with the
  participants (see instructor guide for more details).
- This is a good example text: <https://www.gutenberg.org/ebooks/24542>
- When showing how to add a collaborator, also show how to unwatch a repo.
```


---

## Step 1: Learn how to add collaborators to your repository

Now we know how to share repositories and the first step to allow changes by
others would be to add your group members or collaborators as "collaborators"
under GitHub.  This allows them to change things directly (but we'll
actually do it with review).

- Instructor adds one or two learners who volunteer to later contribute a change via screen sharing.
- You can try this with one of the repositories which we created in the earlier episodes.
- Click on "Settings" (top right), then "Manage access" (left), then "Invite a collaborator" (green button).

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

**Exercise**: We will practice this by suggesting a change in a recipe book:

- Instructor shares an example repository and adds a volunteer learner as collaborator
- Learner shares screen and edits `recipes.txt` via web (click on the edit pen)
- We modify or extend one recipe from the example repository together by guiding the volunteer learner
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
>   **We recommend this for group repositories**.
>   Discuss the advantages/disadvantages of this.
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

```{instructor-note}
- "Non-talking instructor" prepares a conflicting commit during session (check
  what the first PR does).
- Conflict can be shown as demo.
```

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
