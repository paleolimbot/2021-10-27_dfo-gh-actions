# 2021-10-27_dfo-gh-actions

GitHub Actions is a way to run code on somebody else's computer. You can run code on a scheduled basis or when specific actions occur (the most common event is when you push your changes to GitHub. A few examples:

- Checking an R package on every commit: [action](https://github.com/ArgoCanada/argodata/blob/master/.github/workflows/check-release.yaml), [output](https://github.com/ArgoCanada/argodata/runs/3886786612?check_suite_focus=true#step:7:25)
- Checking a Python package on every commit: [action](https://github.com/ArgoCanada/argopandas/blob/master/.github/workflows/check.yaml), [output](https://github.com/ArgoCanada/argopandas/runs/3814636575?check_suite_focus=true#step:7:1)
- Render a website: [action](https://github.com/ArgoCanada/blog/blob/master/.github/workflows/render-distill.yaml), [output](https://github.com/ArgoCanada/blog/runs/3976496975?check_suite_focus=true#step:6:1)
- Run a script on a scheduled basis: [action](https://github.com/paleolimbot/bsrto/blob/master/.github/workflows/build-stable.yaml#L8-L9)

GitHub Actions are YAML files that live in the ".github/workflows" directory of a GitHub repository. To practice, [make a fork of this repository](https://github.com/paleolimbot/2021-10-27_dfo-gh-actions/fork) and then open up the ".github/workflows/hello-world-action.yml" file. The file looks like this:

```yaml

```

## Resources

A few links to official and unofficial guides:

- [Overview from GitHub](https://github.com/features/actions)
- [Full documentation from GitHub](https://docs.github.com/en/actions)
- [Resources for GitHub Actions specific to R](https://github.com/r-lib/actions#additional-resources)
