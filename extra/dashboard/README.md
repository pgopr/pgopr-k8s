# dashboard

The following installs and runs the Kubernetes [dashboard](https://github.com/kubernetes/dashboard) application.

It requires [helm](https://github.com/helm/helm/releases) to be installed and in your path. For example

```bash
$ curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-4
$ chmod 700 get_helm.sh
$ ./get_helm.sh
```

Then install the dashboard by

``` bash
helm repo add kubernetes-dashboard https://kubernetes.github.io/dashboard/
helm upgrade --install kubernetes-dashboard kubernetes-dashboard/kubernetes-dashboard --create-namespace --namespace kubernetes-dashboard
kubectl -n kubernetes-dashboard port-forward svc/kubernetes-dashboard-kong-proxy 8443:443
```

Create the admin account

```bash
kubectl create -f dashboard-serviceaccount.yaml
kubectl create -f dashboard-clusterrolebinding.yaml
```

## Access

Get the token

```bash
kubectl -n kubernetes-dashboard create token admin-user
```

Goto [localhost:8443](http://localhost:8443/) and use the token login
