# traefik

This is a quick demo to get a successful curl against in ingress object with a dummy service. This should work in a Windows Rancher Desktop configuration
that is backed by WSL.

## Using Traefix Ingress Controller

Tutorial is found on [rancher's webiste](https://docs.rancherdesktop.io/how-to-guides/traefik-ingress-example)

### Run it

```bash
kubectl create namespace demo
./demo.sh
curl -vvv http://whoami.docker.localhost/
# * Host whoami.docker.localhost:80 was resolved.
# * IPv6: ::1
# * IPv4: 127.0.0.1
# *   Trying [::1]:80...
# * Connected to whoami.docker.localhost (::1) port 80
# > GET / HTTP/1.1
# > Host: whoami.docker.localhost
# > User-Agent: curl/8.5.0
# > Accept: */*
# > 
# < HTTP/1.1 200 OK
# < Content-Length: 423
# < Content-Type: text/plain; charset=utf-8
# < Date: Mon, 22 Sep 2025 18:40:32 GMT
# < 
# Hostname: whoami-55dd44b4d9-x5bcf
# IP: 127.0.0.1
# IP: ::1
# IP: 10.42.0.16
# IP: fe80::4c78:d3ff:fe1f:c415
# RemoteAddr: 10.42.0.8:57736
# GET / HTTP/1.1
# Host: whoami.docker.localhost
# User-Agent: curl/8.5.0
# Accept: */*
# Accept-Encoding: gzip
# X-Forwarded-For: 10.42.0.7
# X-Forwarded-Host: whoami.docker.localhost
# X-Forwarded-Port: 80
# X-Forwarded-Proto: http
# X-Forwarded-Server: traefik-c98fdf6fb-fg898
# X-Real-Ip: 10.42.0.7

# * Connection #0 to host whoami.docker.localhost left intact
```