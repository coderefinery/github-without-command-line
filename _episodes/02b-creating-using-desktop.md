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

We will exercise sharing a data file in CSV (comma-separated values) format.
For this we either need to create one:
- Create a spreadsheet with Excel/LibreOffice or similar, containing some fantasy data
- Export the spreadsheet to CSV format

You can also share an existing one.

If you don't feel like creating a new CSV file, you can download an example:
- [https://github.com/coderefinery/github-without-command-line/blob/gh-pages/data/academy-award-female.csv](https://github.com/coderefinery/github-without-command-line/blob/gh-pages/data/academy-award-female.csv)
- Click on "Raw", then right-click and "Save as..."

---

### Step 2: Initialize a repository with GitHub Desktop

- Start GitHub Desktop
- Click on "+ Create a New Repository on your hard drive..."

<img src="{{ site.baseurl }}/img/creating-desktop/before-create.png" width="600px" style="border:2px solid #000000;">

<img src="{{ site.baseurl }}/img/creating-desktop/creating.png" width="600px" style="border:2px solid #000000;">

---

### Step 3: Commit the CSV data file

- Copy your (own or downloaded) CSV file to the repository folder
- Note how GitHub desktop changed and shows you the changes
- Make a commit

<img src="{{ site.baseurl }}/img/creating-desktop/diff-before-commit.png" width="600px" style="border:2px solid #000000;">

---

### Step 4: Publish the repository on GitHub

- Browse the history (click "History")
- Click "Publish repository"
- You can choose between a private and a public repository

<img src="{{ site.baseurl }}/img/creating-desktop/publish.png" width="600px" style="border:2px solid #000000;">

---

### Step 5: Create a branch, commit to it, and share it

- Make a change to the CSV file, but do not commit yet
- Observe the change you made in GitHub Desktop before committing
- Create a new branch
- Commit to the new branch
- Publish the new branch to GitHub
- Browse your branches and changes on GitHub

---

### Step 6: Fetch and pull changes from the web

- Edit the file via the GitHub web interface and commit there
- Switch to GitHub Desktop
- Click "Fetch origin"
- Click "Pull origin"

<img src="{{ site.baseurl }}/img/creating-desktop/pull-origin.png" width="600px" style="border:2px solid #000000;">

- Browse the "History" in GitHub Desktop

<img src="{{ site.baseurl }}/img/creating-desktop/after-pull.png" width="600px" style="border:2px solid #000000;">
