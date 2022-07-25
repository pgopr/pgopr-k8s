# minikube

You will need [minikube](https://minikube.sigs.k8s.io/) 1.26 or higher.

Using the latest version is recommended.

## Download

How to download minikube is described [here](https://minikube.sigs.k8s.io/docs/start/).

You will need [kubectl](https://kubernetes.io/docs/tasks/tools/) as well.

## Requirements

* [podman](https://podman.io/)
* [CRI-O](https://cri-o.io/)

## Configuration

Root-less setup with [podman](https://podman.io/) and [CRI-O](https://cri-o.io/).

``` bash
minikube config set driver podman
minikube config set container-runtime cri-o
minikube config set rootless true
```

## Run

``` bash
minikube start
```

## 1 control-plane with 4 workers

``` bash
minikube start -n 4
```

See the minikube [documentation](https://minikube.sigs.k8s.io/docs/handbook/config/) for further options.
