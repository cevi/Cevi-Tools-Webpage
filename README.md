# Cevi Tools Webpage

This repo contains the content of the [cevi.tools](https://cevi.tools/) webpage. Cevi Tools is a collection of useful
tools developed by the Cevi community.

## Local Development (using Docker)

You can preview your changes locally using docker. Clone the Repo, install docker and run:

```bash
docker compose watch
```

The preview page can be accessed on http://localhost:4000.

## Local Development (with local ruby installation)

1) Clone the repo to a local folder
2) Install jekyll following the instructions on the [official webpage](https://jekyllrb.com/docs/installation/).
3) Install your bundles once by running the following commands:

```bash
$ bundle config set --local path 'vendor/bundle'
$ bundle install
```

4) Serve the webpage locally by running the following command:

```bash 
$ bundle exec jekyll serve
```

## Deployment

Our [webpage](https://cevi.tools/) gets served directly from the gh-pages branch, which contains the plain HTML and CSS source. Those files are generated automatically upon committing to the main branch by a GitHub-Action script. Therefore, you do not want to commit directly to the gh-pages branch.
 
For every pull request (to the main branch), GitHub Actions will create a preview such that you can check your changes before releasing them by merging your changes into main.

```
                       ┌───────────────┐              ┌───────────────┐
                       │               │   merge      │               │
    your code ───────► │  pull request │ ───────────► │  main branch  │
     changes           │               │              │               │
                       └───────┬───────┘              └───────┬───────┘
                               │                              │  
                               │                              │  generates sources
                               │                              │  automatically using
                               ▼                              │  a GitHub-Action script
                                                              │
                      generates a preview                     ▼
                        using Firebase                ┌───────────────┐            ┌──────────────┐
                                                      │               │            │              │
                                                      │    gh pages   │  codebase  │    webpage   │
                                                      │     branch    │    for     │  cevi.tools  │
                                                      │               │ ◄────────► │              │
                                                      └───────────────┘            └──────────────┘
```
