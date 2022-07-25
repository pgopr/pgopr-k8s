# kind

You will need [kind](https://kind.sigs.k8s.io/) 0.14 or higher.

Using the latest version is recommended.

## Download

How to download kind is described [here](https://kind.sigs.k8s.io/docs/user/quick-start/#installing-from-release-binaries).

You will need [kubectl](https://kubernetes.io/docs/tasks/tools/) as well.

## Requirements

* [podman](https://podman.io/)

## Run

``` bash
kind create cluster
```

## 1 control-plane with 4 workers

``` bash
kind create cluster --config=kind-cluster.yaml
```

See the kind [documentation](https://kind.sigs.k8s.io/docs/user/configuration/) for further options.
