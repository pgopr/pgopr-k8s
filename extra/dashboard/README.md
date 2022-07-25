# dashboard

The following installs and runs the Kubernetes [dashboard](https://github.com/kubernetes/dashboard) application.

``` bash
kubectl create -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.6.0/aio/deploy/alternative.yaml
kubectl apply -f dashboard-serviceaccount.yaml
kubectl apply -f dashboard-clusterrolebinding.yaml
kubectl -n kubernetes-dashboard get secret $(kubectl -n kubernetes-dashboard get sa/admin-user -o jsonpath="{.secrets[0].name}") -o go-template="{{.data.token | base64decode}}"
kubectl port-forward -n kubernetes-dashboard service/kubernetes-dashboard 8080:80
```

## Access

Goto [localhost:8080](http://localhost:8080/) and use the token login
