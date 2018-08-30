# Augury charts repo

This repository contains augury's helm-charts.

### How it works

GitHub Pages is set to point to `docs` folder. 
Adding new chart is done as follows:

```console
$ helm create mychart
$ # define chart contents
$ helm package mychart
$ mv mychart-<version>.tgz docs
$ # update index.yaml
$ helm repo index docs --url https://augurysys.github.io/charts
$ # commit changes, push, and open PR
```
