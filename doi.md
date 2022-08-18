# Making your project citable

> ## Discussion: is depositing your data/code on GitHub enough?
>
> - Consider the aspect of findability 5 or 10 years from now.
> - What could go wrong?
{: .discussion}

There are many services where you can share or archive your code and data:
See for instance our
[lesson on reproducible research](https://coderefinery.github.io/reproducible-research/03-sharing/#services-for-sharing-and-collaborating-on-research-data).

In this present lesson we will discuss one of the many options to get a **digital object identifier (DOI)**
for your dataset or code:
[Zenodo](https://zenodo.org/), A general-purpose open access repository
created by [OpenAIRE](https://www.openaire.eu/) and CERN.
[Zenodo](https://zenodo.org/) has nice **integration with GitHub**,
and allows researchers to upload files up to 50 GB.

> ## We will exercise in the Zenodo sandbox
>
> We will practice on [https://sandbox.zenodo.org/](https://sandbox.zenodo.org/)
> and not on the "real" [https://zenodo.org/](https://zenodo.org/)
> to make sure we do not create "real" DOIs which we cannot remove.
>
> The sandbox service is useful to calibrate your setup until you are happy with the result
> and then you can go for the real service. Once a dataset is uploaded to the "real" service,
> it cannot be easily removed or modified again (and this is good, otherwise DOIs would not make much sense).
{: .discussion}

---

## Step 1: Prepare an example repository

Through web:
- Create a new repository on GitHub
- Upload some example data into it

Or using GitHub Desktop:
- Create a new repository
- Commit some example data
- Publish your example repository to GitHub

Alternatively we can also practice this with one of the repositories we created
earlier in this lesson.

Here I just created a new one:

<img src="{{ site.baseurl }}/img/doi/example-repo.png" width="800px" style="border:2px solid #000000;">

---

## Step 2: Activate the repository on Zenodo (sandbox)

> ## We will exercise in the Zenodo sandbox
>
> We will practice on [https://sandbox.zenodo.org/](https://sandbox.zenodo.org/)
> and not on the "real" [https://zenodo.org/](https://zenodo.org/)
> to make sure we do not create "real" DOIs which we cannot remove.
{: .discussion}

- Visit <https://sandbox.zenodo.org/account/settings/github/>:

<img src="{{ site.baseurl }}/img/doi/zenodo.png" width="600px" style="border:2px solid #000000;">

- Select the repository you wish to preserve:

<img src="{{ site.baseurl }}/img/doi/switch.png" width="600px" style="border:2px solid #000000;">

- If it is not there, you may need to "Sync now ...":
<img src="{{ site.baseurl }}/img/doi/sync-now.png" width="400px" style="border:2px solid #000000;">

---

## Step 3: Create a "release" and get a DOI

- Go back to the webpage of your GitHub repository
- Click on "releases":

<img src="{{ site.baseurl }}/img/doi/releases.png" width="800px" style="border:2px solid #000000;">

- Fill out the form and click on "Publish release":

<img src="{{ site.baseurl }}/img/doi/publish-release.png" width="600px" style="border:2px solid #000000;">

- Finally reload <https://sandbox.zenodo.org/account/settings/github/>
- It can take few moments for the project to be deposited
- After a while it turns to this:

<img src="{{ site.baseurl }}/img/doi/zenodo-published.png" width="600px" style="border:2px solid #000000;">

---

## Step 4: Add a DOI badge to your repository

This is bonus but for visitors of your GiHub repository it can be nice to find a badge
in your README that informs them about and links to the preserved dataset/code on Zenodo.

- On Zenodo, click on the badge (last figure) which opens up:

<img src="{{ site.baseurl }}/img/doi/zenodo-badge.png" width="600px" style="border:2px solid #000000;">

- Try to add such a badge to your README for the exercise repository:

<img src="{{ site.baseurl }}/img/doi/github-badge.png" width="800px" style="border:2px solid #000000;">
