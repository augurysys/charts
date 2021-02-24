# Augury charts repo - PUBLIC

This repository contains augury's helm-charts.

### How it works

GitHub Pages is set to point to `docs` folder.
Adding new chart is done as follows:

```console
$ helm create mychart # for new charts only
$ # define chart contents
$ helm package mychart
$ mv mychart-<version>.tgz docs
$ # update index.yaml
$ helm repo index docs --url https://augurysys.github.io/charts
$ # commit changes, push, and open PR
```
In addition, the chart should be uploaded to gcs augury helm-repo (for ODEs)
```
$ cd docs
$ helm gcs push mychart-<version>.tgz augury
```
