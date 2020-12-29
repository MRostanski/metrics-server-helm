# metrics-server-helm
Yet another metrics-server helm chart

## Introduction

Yet another metrics-server chart. I am tired of all `kubectl apply`.

## Installation

[Helm](https://helm.sh/) must be installed to use the charts. Please refer to Helm's [documentation](https://helm.sh/docs/) to get started.

Once Helm is set up properly, add the repo as follows:

```bash
helm repo add metrics-server-helm https://mrostanski.github.io/metrics-server-helm
```

Metrics-server can now be installed with the following command:

```bash
helm install metrics-server --namespace kube-system metrics-server-helm/metrics-server
```

If you have custom options or values you want to override:

```bash
helm install metrics-server --namespace kube-system -f my-values.yaml metrics-server-helm/metrics-server
```

Specific versions of the chart can be installed using the --version option, with the default being the latest release. What versions are available for installation can be listed with the following command:

```bash
helm search repo metrics-server-helm
```
