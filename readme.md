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

## Chart Requirements

| Repository | Name | Version |
|------------|------|---------|
| @stable | mysql | 0.12.0 |

## Chart Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| api | bool | `true` | Enable Generatedata API |
| image.pullPolicy | string | `"IfNotPresent"` | Image pull policy |
| image.repository | string | `"mvisonneau/generatedata"` | Image name |
| image.tag | string | `"3.4.1"` | Image tag |
| ingress.annotations | object | `{}` | Ingress annotations |
| ingress.enabled | bool | `true` | Enable ingress |
| ingress.hosts[0].host | string | `"example.com"` | Ingress host |
| ingress.hosts[0].paths[0] | string | `"/"` | Ingress path |
| ingress.tls | object | `{}` | TLS for ingress |
| mysql.enabled | bool | `true` | Enable built-in MySQL |
| mysql.imageTag | string | `"5.7.14"` | MySQL version |
| mysql.mysqlDatabase | string | `"generatedata"` | Database name |
| mysql.mysqlHost | string | `""` | Database host |
| mysql.mysqlPassword | string | `"secret"` | Database password |
| mysql.mysqlRootPassword | string | `"secret"` | Database root password |
| mysql.mysqlTablePrefix | string | `"gd_"` | Database table prefix |
| mysql.mysqlUser | string | `"generatedata"` | Database user |
| mysql.persistence.enabled | bool | `true` | Enable persistence for database |
| mysql.persistence.existingClaim | string | `""` | Existing PVC for database |
| mysql.persistence.size | string | `"1Gi"` | Database disk size |
| mysql.resources | object | `{}` | Databaser Resources |
| replicaCount | int | `1` | Number of replicas  |
| resources | object | `{}` | Compute Resources  |
| salt | string | `"secret"` | Encryption Salt |