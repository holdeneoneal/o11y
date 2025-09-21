# argocd

This directory holds relevant information about the argocd installation.

## Traefik

### Disable TLS

The `argocd-cmd-params-cm` configmap is modified to disable TLS for the argocd API server.
This is per the argocd [documentation to deploy with Traefik](https://argo-cd.readthedocs.io/en/stable/operator-manual/ingress/#traefik-v30).