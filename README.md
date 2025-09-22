# o11y

This repo assumes that the consumer is using a local k3s cluster with Traefik ingress controller repository. This repo will hold a set of assets and installation instructions to achieve the following:

- Install ArgoCD
- Use ArgoCD to deploy and manage Grafana Alloy
- Provide configuration for Grafana Alloy to send telemetry data about the cluster and any applications deployed to Grafana Cloud

Stretch goals:

- Deploy Gateway API and use that to access ArgoCD UI and API
- Setup a second cluster and have ArgoCD deploy apps across clusters, with Alloy monitoring both.
