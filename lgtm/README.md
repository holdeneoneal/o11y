# lgtm

This directory holds the information needed to deploy the LGTM(Grafana, Loki, Tempo, Mimir).

## Deployment

### Helm

The community maintained [lgtm helm chart](https://github.com/grafana/helm-charts/tree/main/charts/lgtm-distributed)
will be deployed via ArgoCD.

### Configuration

This directory holds the `values.yaml` file that will be used to configure the deployment

## NOTES

- The app gets out of sync due to the admin password being updated. I think it's updated automatically during the deployment by some controller in the chart.
  - Workarounds:
    - Use the `ignoreDifferences` field in the app to silence the Secret issues
    - Create a secret for the creds and have it use those by overriding