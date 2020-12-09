# ECK Operator

Elastic Cloud on Kubernetes (ECK) Operator chart.

Originally sourced from [upstream](https://github.com/elastic/cloud-on-k8s/tree/master/deploy/eck-operator), and minimally modified.

## Contents

[Developer Guide](docs/developer-guide.md)

## Deployment
```
git clone https://repo1.dsop.io/platform-one/big-bang/apps/core/eck-operator.git
cd eck-operator/chart

helm dependency update

helm install eck-operator chart 
```

