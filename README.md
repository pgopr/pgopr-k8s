# pgopr-k8s: Kubernetes files for the pgopr operator

`pgopr` is a Kubernetes operator that controls a PostgreSQL cluster and related technologies on Kubernetes 1.23+.

This repository contains Kubernetes files that will help to setup a development environment.

## 

1. Use `kubectl apply -f echoes.example.com.yaml` to create the CustomResourceDefinition inside Kubernetes.
1. Build the project with `cargo build`. If the build fails, make sure `libssl-dev` is available.
1. Run the operator using `cargo run`. It will run outside of the Kubernetes cluster and connect to the Kubernetes REST API using the account inside the `KUBECONFIG` automatically.

Finally, a custom `Echo` resource can be created with `kubectl apply -f echo-example.yaml`. A new deployment of two pods with `Echo` REST API service will be created. This can be checked with the `kubectl get pods` or `kubectl get deployments` command.






## Requirements

* [Kubernetes](https://kubernetes.io/) 1.23+

## Runtime platforms

* [kind](https://kind.sigs.k8s.io/) 0.12+
* [minikube](https://minikube.sigs.k8s.io/docs/) 1.26+

## Contributing

Contributions to `pgopr` are managed on [GitHub.com](https://github.com/pgopr/pgopr-k8s/)

* [Ask a question](https://github.com/pgopr/pgopr-k8s/discussions)
* [Raise an issue](https://github.com/pgopr/pgopr-k8s/issues)
* [Feature request](https://github.com/pgopr/pgopr-k8s/issues)
* [Code submission](https://github.com/pgopr/pgopr-k8s/pulls)

Contributions are most welcome !

Please, consult our [Code of Conduct](./CODE_OF_CONDUCT.md) policies for interacting in our
community.

Consider giving the project a [star](https://github.com/pgopr/pgopr-k8s/stargazers) on
[GitHub](https://github.com/pgopr/pgopr-k8s/) if you find it useful.

## License

[Eclipse Public License - v2.0](https://www.eclipse.org/legal/epl-2.0/)
