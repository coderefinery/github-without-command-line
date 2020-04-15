---
layout: episode
title: Creating repositories using GitHub Desktop
teaching: 20
exercises: 0
questions:
  - Creating and pushing local repositories.
  - How to record (commit) changes.
  - Inspecting changes before they are committed.
  - Browsing changes.
objectives:
  - ...
---

## Creating repositories using GitHub Desktop

We will practice creating a new repository using GitHub Desktop, committing
changes to it, browsing the changes, creating branches, and more.
This is practically the same as the previous episode, but we introduce
some new concepts:

- There is now two copies of your repository: that on your computer,
  and that on Github.
- We introduce the concepts of **pull** and **fetch** to move code
  Github→local, and **push** to move code local→Github.
- **Github Desktop** is a application that lets you manage files with
  git. It is *not* the only way to use git, but it is easy and
  integrated, so it's a nice thing to teach.

In small groups it can be useful to do this side by side (in-person) or one
learner shares their screen (video) and others can ask questions and give
suggestions. In a larger group the instructor can demonstrate these and then
participants can try on their own and then ask questions.

- [Step 1: Create an example spreadsheet](#step-1-create-an-example-spreadsheet)
- [Step 2: Initialize a repository with GitHub Desktop](#step-2-initialize-a-repository-with-github-desktop)
- [Step 3: Commit the CSV data file](#step-3-commit-the-csv-data-file)
- [Step 4: Publish the repository on GitHub](#step-4-publish-the-repository-on-github)
- [Step 5: Create a branch, commit to it, and share it](#step-5-create-a-branch-commit-to-it-and-share-it)
- [Step 6: Fetch and pull changes from the web](#step-6-fetch-and-pull-changes-from-the-web)

---

### Step 1: Create an example spreadsheet

In this exercise, we will share a data file in CSV (comma-separated
values) format and see how Github nicely displays it.  First, step, we
need to make some CSV file.

Either create a new CSV file:
- Create a spreadsheet with Excel/LibreOffice or similar, containing some fantasy data
- Export the spreadsheet to CSV format

You can also share an existing one.

If you don't feel like creating a new CSV file, you can download an example:
- [https://github.com/coderefinery/github-without-command-line/blob/gh-pages/data/academy-award-female.csv](https://github.com/coderefinery/github-without-command-line/blob/gh-pages/data/academy-award-female.csv)
- Click on "Raw", then right-click and "Save as..."

Make sure the file is actually in CSV format, not Excel/spreadsheet
format.  That will work with git, but all you can do is download it.

---

### Step 2: Initialize a repository with GitHub Desktop

First, we make a new local repository.  At this stage, github.com
doesn't know anything about it.

- Start GitHub Desktop
- Click on "+ Create a New Repository on your hard drive..."

<img src="{{ site.baseurl }}/img/creating-desktop/before-create.png" width="600px" style="border:2px solid #000000;">

<img src="{{ site.baseurl }}/img/creating-desktop/creating.png" width="600px" style="border:2px solid #000000;">

---

### Step 3: Commit the CSV data file

Now, we add the CSV to git.  First, we put it in the git directory,
then tell git to save it.

- Copy your (own or downloaded) CSV file to the repository folder
- Note how GitHub desktop changed and shows you the changes
- Make a commit

<img src="{{ site.baseurl }}/img/creating-desktop/diff-before-commit.png" width="600px" style="border:2px solid #000000;">

---

### Step 4: Publish the repository on GitHub

This is the step where we actually upload it to Github.  Github
Desktop lets us create a new repository on github.com without using
the web browser.  In this step, we also **push** the changes to the
**remote** repository, though it happens without us seeing all the
middle steps.

- Browse the history (click "History")
- Click "Publish repository"
- Don't use the same name as the previous episode: you'll get a
  conflict.
- You can choose between a private and a public repository

<img src="{{ site.baseurl }}/img/creating-desktop/publish.png" width="600px" style="border:2px solid #000000;">

---

### Step 5: Create a branch, commit to it, and share it

This is pretty much the normal work: edit a file, commit it.  But, in
this case, we are going to commit it to a new branch.  Why?  We'll see
later.

- Make a change to the CSV file, but do not commit yet
- Observe the change you made in GitHub Desktop before committing
- Create a new branch
- Commit to the new branch
- Publish the new branch to GitHub
- Browse your branches and changes on GitHub

---

### Step 6: Fetch and pull changes from the web

Now we show how to **pull** code from Github→local.

- Edit the file via the GitHub web interface and commit there
- Switch to GitHub Desktop
- Click "Fetch origin"
- Click "Pull origin"

<img src="{{ site.baseurl }}/img/creating-desktop/pull-origin.png" width="600px" style="border:2px solid #000000;">

- Browse the "History" in GitHub Desktop

<img src="{{ site.baseurl }}/img/creating-desktop/after-pull.png" width="600px" style="border:2px solid #000000;">

What's the difference between **fetch** and **pull**?  Fetch gets the
changes, but doesn't make them active.  Pull = fetch + make changes
active in your current repository (does a **merge** which we will
discuss later).

---

> ## Summary
>
> With Github Desktop, we can do everything we can on the web, but it's
> more natural.  The most important concepts are that of **remotes**
> (links between repositories), **pushing**, and **pulling**.
>
> We don't cover it in this workshop, but you can eventually do all of
> these things from the command line, for example `git commit
> some_file.csv`.  Once you are doing many things, this can be faster.
> Still, there's almost always a place for applications like this to
> make things smoother.
{: .discussion}
