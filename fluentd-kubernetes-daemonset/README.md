# fluentd-kubernetes-daemonset
[![Circle CI](https://circleci.com/gh/augurysys/fluentd-kubernetes-daemonsetsvg?style=svg&circle-token=0d00d6c2e7b35ac108f7ffa87bdba2270da62d09)](https://circleci.com/gh/augurysys/fluentd-kubernetes-daemonset)

This repository for fluentd-kubernetes-daemonset helm chart.
Used for shipping kubernetes apps logs to logentries.

# Development

Prerequisites:

1. [`asdf-vm`](https://github.com/asdf-vm/asdf)

Development cycle:

1. To install the current tools versions run: `asdf install`
1. create a feature branch
1. make changes
1. check the changes, if they are good, create a PR


# Deployment

Prerequisites:

Assign cluster-admin role to triller

```bash
$ kubectl create serviceaccount -n kube-system tiller
$ kubectl create clusterrolebinding tiller-binding --clusterrole=cluster-admin --serviceaccount kube-system:tiller
```
