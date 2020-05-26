## Helm chart for generatedata

## Prerequisites

- Kubernetes 1.4+
- [helm](https://helm.sh)

## Installing the Chart

To install the chart:

```console
$ helm dependency update
$ helm install generatedata --wait .
```

> **Tip**: List all releases using `helm list`

## Updating the Chart

To update the chart:

```console
$ helm dependency update
$ helm upgrade generatedata --wait .
```

## Uninstalling the Chart

To uninstall/delete:

```console
$ helm delete generatedata
```

### The following table lists the configurable parameters of the generatedata chart and their default values.

| Parameter           | Description                                 | Default            |
|---------------------|---------------------------------------------|--------------------|
| replicaCount        | Number of replicas                  | 1                          |
| image.repository    | Image name                          |"mvisonneau/generatedata"   |
| image.tag           | Image tag                           | "3.4.1"                    |
| image.pullPolicy    | Image pull policy                   | "IfNotPresent"             |
| ingress.annotations | Ingress annotations                 | {}                         |
| ingress.hosts       | Ingress hosts                       | {"example.com"}            |
| ingress.path        | Ingress path                        | "/"                        |
| ingress.tls         | Secrets for tls                     | {}                         |
| resources           | Compute Resources                   | {}                         |