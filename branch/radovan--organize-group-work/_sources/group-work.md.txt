---
layout: episode
title: How to organize a group's work
teaching: 15
exercises: 15
questions:
  - Should I start a repo under my account or open a new organization?
  - Should I add everybody as collaborator?
  - GitHub vs GitLab?
  - What permissions to choose?
  - Pull requests vs direct commits for types of projects
  - Small vs large changes
---

# How to organize a group's work

---

## Step X: Contributing non-trivial changes

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
