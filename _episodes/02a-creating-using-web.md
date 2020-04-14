---
layout: episode
title: Creating repositories using the web interface
teaching: 20
exercises: 0
questions:
  - Creating repositories on GitHub.
  - How to record (commit) changes.
  - Browsing changes.
  - Repository insights and settings.
objectives:
  - ...
---

## Creating repositories using the web interface

We will practice creating a new repository using the web interface, committing
changes to it, browsing the changes, creating branches, and more.

In small groups it can be useful to do this side by side (in-person) or one
learner shares their screen (video) and others can ask questions and give
suggestions. In a larger group the instructor can demonstrate these and then
participants can try on their own and then ask questions.

- [Step 1: Create a repository with a README and a license](#step-1-create-a-repository-with-a-readme-and-a-license)
- [Step 2: Create a new file](#step-2-create-a-new-file)
- [Step 2: Modify a file](#step-2-modify-a-file)
- [Step 4: Create a new branch](#step-4-create-a-new-branch)
- [Step 5: Repository insights and settings](#step-5-repository-insights-and-settings)
- [Step 6: Adding a license to an existing repository](#step-6-adding-a-license-to-an-existing-repository)
- [Discussion: How can we merge branches?](#discussion-how-can-we-merge-branches)

---

### Step 1: Create a repository with a README and a license

Make sure that you are **logged into GitHub**.

To create a repository we either click the green button "New" (top left corner):
<img src="{{ site.baseurl }}/img/creating-web/new-top-left.png" width="400px" style="border:2px solid #000000;">

---

Or if you see your profile page, there is a "+" menu (top right corner):
<img src="{{ site.baseurl }}/img/creating-web/new-top-right.png" width="400px" style="border:2px solid #000000;">

---

Yet another way to create a new repository is to visit
[https://github.com/new](https://github.com/new) directly.

---

We then land at the following form.  Please fill it out and set **Initialize
this repository with a README** and choose a license.  If you don't find a
suitable license, we will show later how you can add your own.

<img src="{{ site.baseurl }}/img/creating-web/form.png" width="600px" style="border:2px solid #000000;">

---

And now we have a repository with a README and LICENSE and one commit:

<img src="{{ site.baseurl }}/img/creating-web/created.png" width="600px" style="border:2px solid #000000;">

---

### Step 2: Create a new file

Create a file, e.g. `guacamole.md` (the "md" ending signals that this is in Markdown format):
<img src="{{ site.baseurl }}/img/creating-web/new-file-buttons.png" width="400px" style="border:2px solid #000000;">

In the new file you can share your favorite cooking recipe (or something else):
<img src="{{ site.baseurl }}/img/creating-web/new-file-editor.png" width="400px" style="border:2px solid #000000;">

Then add a commit message and commit (save):

<img src="{{ site.baseurl }}/img/creating-web/new-file-commit.png" width="600px" style="border:2px solid #000000;">

> ## Discussion: Good commit messages
>
> - What has changed is more useful than which file has changed
> - Sometimes we forget to document *why* something was changed
> - Many projects start out as projects "just for me" and end up to be successful projects
>   that are developed by 50 people over decades.
> - Write commit messages in English that will be understood
>   15 years from now by someone else than you.
> - ["My favourite Git commit"](https://fatbusinessman.com/2019/my-favourite-git-commit)
> - ["On commit messages"](https://who-t.blogspot.com/2009/12/on-commit-messages.html)
> - ["How to Write a Git Commit Message"](https://chris.beams.io/posts/git-commit/)
{: .discussion}

---

### Step 2: Modify a file

Now improve the recipe by adding an ingredient or an instruction step:
- Click on the file.
- Click the "pen" icon on top right ("edit this file").

Make an improvement, write a commit message, commit:
<img src="{{ site.baseurl }}/img/creating-web/edit-file-preview.png" width="400px" style="border:2px solid #000000;">

Once you have done that, browse your commits:
<img src="{{ site.baseurl }}/img/creating-web/commits-browse.png" width="300px" style="border:2px solid #000000;">

In my example I got:

<img src="{{ site.baseurl }}/img/creating-web/commits-example.png" width="800px" style="border:2px solid #000000;">

---

### Step 4: Create a new branch

- Create a new branch:
  <img src="{{ site.baseurl }}/img/creating-web/create-branch.png" width="400px" style="border:2px solid #000000;">
- Modify your recipe on the newly created branch.
- Then switch back to the `master` branch and browse your recipe there.

---

### Step 5: Repository insights and settings

Have a look at the network, hover over the dots in the graph (commits):

<img src="{{ site.baseurl }}/img/creating-web/network.png" width="800px" style="border:2px solid #000000;">

---

### Step 6: Adding a license to an existing repository

This is an optional step to show how we can add a license
to an existing repository.

- Visit [https://choosealicense.com/](https://choosealicense.com/) and let it guide you.
- If you don't find a suitable license,
  choose among [https://choosealicense.com/appendix/](https://choosealicense.com/appendix/).
- Once you have chosen, click on the license name, and you can enter your GitHub repository URL (top right)
  which will open a pull request (change request) to the repository:

<img src="{{ site.baseurl }}/img/creating-web/choosealicense.png" width="800px" style="border:2px solid #000000;">

---

### Discussion: How can we merge branches?

First browse to the overview of all branches:
<img src="{{ site.baseurl }}/img/creating-web/branches-click.png" width="400px" style="border:2px solid #000000;">

Now to initiate a merge, click on "New pull request":

<img src="{{ site.baseurl }}/img/creating-web/branches-overview.png" width="800px" style="border:2px solid #000000;">

We will return to "pull requests" when we later discuss how to contribute
changes.
