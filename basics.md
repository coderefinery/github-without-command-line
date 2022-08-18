# Basics and motivation

```{questions}
- What is version control and why?
- What are commits and branches?
- What are forks and clones?
```

```{objectives}
- Get a mental representation for commits and branches.
- Understand the difference between forks and clones.
- Understand the difference between Git and GitHub.
```

> ## What we will not cover
>
> - Command line interface
> - Cloning using SSH protocol and SSH keys
> - Rebasing and squashing
> - Many Git tricks which can be explored later
{: .discussion}


## Version control

### What are version control tools?

- Version control is a tool that can **record snapshots of a project**.
- You can think of version control like regularly taking a photo of your work
  (movie sets take regular polaroids to be able to recreate a scene the next day).

```{figure} /img/basics/commits-snapshots.png
---
class: with-border
---

Snapshots (**commits**) in the [EHT-imaging](https://github.com/achael/eht-imaging) repository.
```


### What we typically like to snapshot

- Software (this is how it started but Git/GitHub can track a lot more)
- Scripts
- Documents (plain text file much better suitable than Word documents)
- Manuscripts (Git is great for collaborating/sharing LaTeX manuscripts)
- Configuration files
- Website sources
- Data


### Why are snapshots valuable? Reproducibility!

- We can always go back if we make a mistake.
- We have the means to refer to a well-defined version of a project when sharing, collaborating, and publishing.
- If we discover a problem, we can find out when it was introduced.

---

## Difference between [Git](https://git-scm.com) and [GitHub](https://github.com)

**Git**
- Tool that can record and synchronize snapshots.
- Not the only tool that can record snapshots (other popular tools are
[Subversion](https://subversion.apache.org) and [Mercurial](https://www.mercurial-scm.org)).
- Not only a tool but also a format that can be read by many different tools.

**GitHub**
- Service that provides hosting for Git repositories with a nice web interface.
- Not the only service that provides this (other popular services are
[GitLab](https://about.gitlab.com/) and [Bitbucket](https://bitbucket.org)).

**GitHub Desktop**
- Graphical user interface to Git and GitHub which runs locally on your computer.
- There are other tools that can do this, too (e.g. [Sourcetree](https://www.sourcetreeapp.com/)).

---

## Commits, branches, repositories, forks, clones

- **repository**: The project, contains all data and history (commits, branches, tags).
- **commit**: Snapshot of the project, gets a unique identifier (e.g. `c7f0e8bfc718be04525847fc7ac237f470add76e`).
- **branch**: Independent development line, often we call the main development line `master`.
- **tag**: A pointer to one commit, to be able to refer to it later. Like a sticky note that you attach to a particular commit (e.g. `phd-printed` or `paper-submitted`).
- **cloning**: Copying the whole repository to your laptop - the first time. It is not necessary to download each file one by one.
- **forking**: Taking a copy of a repository (which is typically not yours) - your
  copy (fork) stays on GitHub and you can make changes to your copy.

```{figure} /img/basics/file-view.png
---
class: with-border
---

GitHub file view of the
[EHT-imaging](https://github.com/achael/eht-imaging)
repository.  This is the version of all files at a single point in
time.
```

```{figure} /img/basics/history-demo.png
---
class: with-border
---

Github history view of the
[EHT-imaging](https://github.com/achael/eht-imaging)
repository.  This is the progression of the repository (with the
**commit message** over time).
```

```{figure} /img/basics/commits-and-branches.svg
---
class: with-border
---

Network graph of all commits in the
[EHT-imaging](https://github.com/achael/eht-imaging/network)
repository.  This shows the relationship between different **forks**
of people who are contributing and sharing code.
```


### Interesting repositories to explore these concepts

- Event Horizon Telescope imaging software
  - Repository: <https://github.com/achael/eht-imaging>
  - Commits, branches, forks: <https://github.com/achael/eht-imaging/network>
- [Activity inequality study](http://activityinequality.stanford.edu/)
  - Contains data and code necessary to create figures from their article.
  - Data: <https://github.com/timalthoff/activityinequality/tree/master/data>
- FiveThirtyEight story [Why We’re Sharing 3 Million Russian Troll Tweets](https://fivethirtyeight.com/features/why-were-sharing-3-million-russian-troll-tweets/)
  - Contains data and readme file, no code.
  - Data: <https://github.com/fivethirtyeight/russian-troll-tweets>
- The NY Times Coronavirus (Covid-19) Data in the United States
  - Contains data, readme, license, but no code.  As of 2020.april,
    being updated every day.
  - Data: <https://github.com/nytimes/covid-19-data>
  - Website: <https://www.nytimes.com/interactive/2020/us/coronavirus-us-cases.html>
- CSV exports of the Getty Provenance Index
  - Data: <https://github.com/thegetty/provenance-index-csv>
- Entire books are written using Git/GitHub:
  - <https://github.com/rust-lang/book>
  - <https://github.com/ropensci/dev_guide>
  - <https://github.com/alan-turing-institute/the-turing-way>
- Papers under open review:
  - <https://github.com/openjournals/joss-reviews/issues>

---

> ## Why using repositories?
>
> - All changes are recorded.
> - We do not have to send changes via email.
> - We can experiment with several ideas which might not work out (using branches).
> - Several people can work on the same project at the same time (using branches).
> - We do not have to wait for others to send us "the latest version" over email.
> - We do not have to merge parallel developments by hand.
> - Group-based access model where shared access is the default, instead of
>   everything fundamentally owned by individuals who manage sharing as-needed:
>   with Git you can easily have collaboration be the default.
> - It is possible to serve websites directly from a repository.
{: .discussion}

> ## Discussion
>
> - How have you solved these in the past without version control?
{: .discussion}
