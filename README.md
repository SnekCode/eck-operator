# eck-operator

![Version: 1.9.1-bb.1](https://img.shields.io/badge/Version-1.9.1--bb.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.9.1](https://img.shields.io/badge/AppVersion-1.9.1-informational?style=flat-square)

A Helm chart for deploying the Elastic Cloud on Kubernetes (ECK) operator: the official Kubernetes operator for orchestrating Elasticsearch, Kibana, APM Server, Enterprise Search, and Beats.

## Upstream References
* <https://github.com/elastic/cloud-on-k8s>

## Learn More
* [Application Overview](docs/overview.md)
* [Other Documentation](docs/)

## Pre-Requisites

* Kubernetes Cluster deployed
* Kubernetes config installed in `~/.kube/config`
* Helm installed

Kubernetes: `>=1.12.0-0`

Install Helm

https://helm.sh/docs/intro/install/

## Deployment

* Clone down the repository
* cd into directory
```bash
helm install eck-operator chart/
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| nameOverride | string | `"elastic-operator"` |  |
| fullnameOverride | string | `"elastic-operator"` |  |
| managedNamespaces | list | `[]` |  |
| installCRDs | bool | `true` |  |
| replicaCount | int | `1` |  |
| image.repository | string | `"registry1.dso.mil/ironbank/elastic/eck-operator/eck-operator"` |  |
| image.tag | string | `"1.9.1"` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| imagePullSecrets | list | `[]` |  |
| resources.limits.cpu | string | `"200m"` |  |
| resources.limits.memory | string | `"256Mi"` |  |
| resources.requests.cpu | string | `"200m"` |  |
| resources.requests.memory | string | `"256Mi"` |  |
| podAnnotations | object | `{}` |  |
| podLabels | object | `{}` |  |
| podSecurityContext.runAsNonRoot | bool | `true` |  |
| securityContext | object | `{}` |  |
| nodeSelector | object | `{}` |  |
| tolerations | list | `[]` |  |
| affinity | object | `{}` |  |
| env | list | `[]` |  |
| volumeMounts | list | `[]` |  |
| volumes | list | `[]` |  |
| createClusterScopedResources | bool | `true` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.name | string | `""` |  |
| tracing.enabled | bool | `false` |  |
| tracing.config.ELASTIC_APM_SERVER_URL | string | `"http://localhost:8200"` |  |
| tracing.config.ELASTIC_APM_SERVER_TIMEOUT | string | `"30s"` |  |
| refs.enforceRBAC | bool | `false` |  |
| webhook.enabled | bool | `true` |  |
| webhook.caBundle | string | `"Cg=="` |  |
| webhook.certManagerCert | string | `nil` |  |
| webhook.certsDir | string | `"/tmp/k8s-webhook-server/serving-certs"` |  |
| webhook.failurePolicy | string | `"Ignore"` |  |
| webhook.manageCerts | bool | `true` |  |
| webhook.namespaceSelector | object | `{}` |  |
| webhook.objectSelector | object | `{}` |  |
| softMultiTenancy.enabled | bool | `false` |  |
| kubeAPIServerIP | string | `nil` |  |
| telemetry.disabled | bool | `false` |  |
| telemetry.distributionChannel | string | `"helm"` |  |
| config.logVerbosity | string | `"0"` |  |
| config.metricsPort | string | `"4321"` |  |
| config.containerRegistry | string | `"docker.elastic.co"` |  |
| config.maxConcurrentReconciles | string | `"3"` |  |
| config.caValidity | string | `"8760h"` |  |
| config.caRotateBefore | string | `"24h"` |  |
| config.certificatesValidity | string | `"8760h"` |  |
| config.certificatesRotateBefore | string | `"24h"` |  |
| config.setDefaultSecurityContext | bool | `true` |  |
| config.kubeClientTimeout | string | `"60s"` |  |
| config.elasticsearchClientTimeout | string | `"180s"` |  |
| config.validateStorageClass | bool | `true` |  |
| podMonitor.enabled | bool | `false` |  |
| podMonitor.labels | object | `{}` |  |
| podMonitor.annotations | object | `{}` |  |
| podMonitor.interval | string | `"5m"` |  |
| podMonitor.scrapeTimeout | string | `"30s"` |  |
| podMonitor.podTargetLabels | list | `[]` |  |
| podMonitor.podMetricsEndpointConfig | object | `{}` |  |
| global.manifestGen | bool | `false` |  |
| global.createOperatorNamespace | bool | `true` |  |
| global.kubeVersion | string | `"1.16.0"` |  |
| license.trial | bool | `false` |  |
| license.keyJSON | string | `""` |  |
| networkPolicies.enabled | bool | `false` |  |
| networkPolicies.controlPlaneCidr | string | `"0.0.0.0/0"` |  |
| monitoring.enabled | bool | `false` |  |
| openshift | bool | `false` |  |
| istio.enabled | bool | `false` |  |
| upgradeCrds.enabled | bool | `false` |  |
| upgradeCrds.image.repository | string | `"registry1.dso.mil/ironbank/big-bang/base"` |  |
| upgradeCrds.image.tag | float | `8.4` |  |

## Contributing

Please see the [contributing guide](./CONTRIBUTING.md) if you are interested in contributing.
