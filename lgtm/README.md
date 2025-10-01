# lgtm

This directory holds the information needed to deploy the LGTM(Grafana, Loki, Tempo, Mimir).

## Deployment

### Helm

The community maintained [lgtm helm chart](https://github.com/grafana/helm-charts/tree/main/charts/lgtm-distributed)
will be deployed via ArgoCD.

### Configuration

This directory holds the `values.yaml` file that will be used to configure the deployment