# K8s Qinglong Longhorn

[K8s](https://kubernetes.io/) + [Qinglong](https://github.com/whyour/qinglong) + [Longhorn](https://longhorn.io/)

## Pre-requisites

- Install Longhorn, Ref: [K8s Alist Longhorn](https://github.com/jerryshell/k8s-alist-longhorn)
- TLS Ingress, Ref: [K8s Traefik cert-manager DNS01 TLS](https://github.com/jerryshell/k8s-traefik-cert-manager-dns01-tls)

## Git clone

```bash
git clone https://github.com/jerryshell/k8s-qinglong-longhorn.git
cd k8s-qinglong-longhorn
```

## Replace k8s/\*.yaml

- `qinglong.jerryshell.eu.org` -> `qinglong.yourdomain.com`

## Apply

```bash
kubectl apply -f k8s/
```

## LICENSE

[GNU Affero General Public License v3.0](https://choosealicense.com/licenses/agpl-3.0/)
