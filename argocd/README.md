# argocd

This directory holds relevant information about the argocd installation.

## Install

```bash
kubectl apply -k ./
sleep 60
kubectl port-forward svc/argocd-server -n argocd 8080:443
```

## Get initial password

```bash
# Grab the initial password
argocd admin initial-password -n argocd
```

## Login with CLI when port-forwarding

```bash
# Relevant issue if trying to use localhost: https://github.com/argoproj/argo-cd/issues/10884
argocd login --username admin --password $argopass --port-forward --plaintext --port-forward-namespace argocd
```

### Update the admin password

```bash
argocd account update-password
```

## Login with Browser

Using your local browser, go to `http://localhost:8080/login`, the
username is `admin`.



## Traefik

### Disable TLS

NOTE: Accessing the argocd install via an ingress is not in scope yet.

The `argocd-cmd-params-cm` configmap is modified to disable TLS for the argocd API server.
This is per the argocd [documentation to deploy with Traefik](https://argo-cd.readthedocs.io/en/stable/operator-manual/ingress/#traefik-v30).