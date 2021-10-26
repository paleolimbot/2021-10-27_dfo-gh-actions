# 2021-10-27_dfo-gh-actions

GitHub Actions is a way to run code on somebody else's computer. You can run code on a scheduled basis or when specific actions occur (the most common event is when you push your changes to GitHub. A few examples:

- Checking an R package on every commit: [action](https://github.com/ArgoCanada/argodata/blob/master/.github/workflows/check-release.yaml), [output](https://github.com/ArgoCanada/argodata/runs/3886786612?check_suite_focus=true#step:7:25)
- Checking a Python package on every commit: [action](https://github.com/ArgoCanada/argopandas/blob/master/.github/workflows/check.yaml), [output](https://github.com/ArgoCanada/argopandas/runs/3814636575?check_suite_focus=true#step:7:1)
- Render a website: [action](https://github.com/ArgoCanada/blog/blob/master/.github/workflows/render-distill.yaml), [output](https://github.com/ArgoCanada/blog/runs/3976496975?check_suite_focus=true#step:6:1)
- Run a script on a scheduled basis: [action](https://github.com/paleolimbot/bsrto/blob/master/.github/workflows/build-stable.yaml#L8-L9)

GitHub Actions are YAML files that live in the ".github/workflows" directory of a GitHub repository. To practice, [make a fork of this repository](https://github.com/paleolimbot/2021-10-27_dfo-gh-actions/fork) and then open up the ".github/workflows/hello-world-action.yaml" file. The file looks like this:

```yaml

```

I'll describe the steps from the bottom up.

- The action produces a pdf document (demo.pdf) from an RMarkdown file (demo.Rmd). This pdf output is made availabe by the "upload artifact" step as a clickable link in the build log.
- The document is rendered using `rmarkdown::render()`.
- Before the document is rendered, the actions needs to install R, install the ability to produce PDF output, and install R packages it needs.

## Your turn 1

Since you've just forked the repository, the action hasn't run for you yet. Update the author name in the document from "Dewey Dunnington" to your own name. You can do this by clicking the "edit" link at the top (no need to clone into your local computer if you don't want to!).

Click "commit changes" at the bottom and wait for your action to complete.

When the action has completed, open the "demo.pdf" artifact to view your results!

## Resources

A few links to official and unofficial guides:

- [Overview from GitHub](https://github.com/features/actions)
- [Full documentation from GitHub](https://docs.github.com/en/actions)
- [Resources for GitHub Actions specific to R](https://github.com/r-lib/actions#additional-resources)
