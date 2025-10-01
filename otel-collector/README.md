# otel-collector

## Deployment

### Helm

The otel-collector is deployed using Helm via ArgoCD, per the [otel documentation](https://opentelemetry.io/docs/platforms/kubernetes/helm/collector/).

The ArgoCD application will point to the public otel collector helm chart.

### Values

This directory holds the `values.yaml` file that will be used by ArgoCD.