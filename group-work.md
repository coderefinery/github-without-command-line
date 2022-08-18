# How to organize a group's work

> ## Discussion
>
> Do you want to work together? What are the benefits? How much of our
> individual work is caused by not having a way to collaborate? If we could
> collaborate, would it improve the quality of our work? Do we want to?"
{: .discussion}


## GitHub organizations

Should I start a repository under my account or open a new organization?
- Single-person projects often start under own account.
- It is no problem to move a project from own namespace to an organization later.
- When starting a larger project with several people, possibly several affiliations, an organization may be a better start.
- If this is a GitHub pages project, then it will matter for the URL:
  `myuser.github.io/myproject/` vs. `ourorg.github.io/ourproject/`.

Should I add everybody as collaborator?
- If you are a handful of project collaborators it probably makes sense to add everybody as collaborators.
- But one does not have to be a *collaborator* to contribute (anybody can send contributions to public projects).
- External contributors don't have to be added.

---

## Organizational permissions

- Organizations have **owners** and **members**.
- Owners can add additional members and delete repositories.
- Members can also be organized into teams.
- We recommend to write-protect the default branch and protect it against force-pushes and accidental deletions.

---

## GitHub or GitLab?

- GitHub: probably better integrations (with services like Zenodo), probably more visibility (more users).
- GitLab: more features, you can also self-host, more advanced continuous integration.
- Your own university's GitLab: most control, local support, but limited visibility and you might lose access when you move on.

---

## Direct commits or pull requests?

- For single-person projects: direct pushes.
- If you have somebody who can help you with code review: use pull requests.
- For projects with 2 or more persons: agree on applying all changes via pull requests
  and create a new branch for every change.
- Do you ever review what others do? Would it improve your work if you did?
  Would it overall save time?

---

## Small vs. large changes

- For larger changes first open an issue and describe your idea and collect feedback.
- Alternative: if you already have a larger change half-finished but you are unsure whether you are on the right
  track, open a **draft pull request**. These are meant to share unfinished drafts and collect suggestions.

---

## Optional exercise contributing larger changes

```{instructor-note}
- A participant shares screen and creates a repository, then instructor takes screen share and
  we go through steps to contribute to that repository (without write permissions), then
  screen share goes back to participant and we together review this change
```

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
