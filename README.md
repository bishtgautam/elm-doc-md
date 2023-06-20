# Overview

This is a test repository to explore options for developing documentation for
the E3SM Land Model. 

- The guide in this repo is written in [Markdown (MD)](https://www.markdownguide.org/).
- [MkDocs](https://www.mkdocs.org/) is used to generate the html pages based on MD.
  - The guide is hosted using Github pages [here](https://bishtgautam.github.io/elm-doc-md/).
- This repo contains two branchs:
  - `main`
  - `gh-pages`: This branch is created by `mkdocs` and is used by Github pages to display the guide

NERSC is using MkDocs for it's documentation (see [https://gitlab.com/NERSC/nersc.gitlab.io/](https://gitlab.com/NERSC/nersc.gitlab.io/)).


# Building the guide

Assuming `mkdocs` is installed on the machine, the html version of the manuscript
can be build locally via

```
mkdocs html
```

Then, `site/index.html` can be opened in a brower to explore the guide. The guide can be
deployed to Github via

```
mkdocs gh-deploy
```
