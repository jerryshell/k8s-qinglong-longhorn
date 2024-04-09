# K8s Qinglong Longhorn

[K8s](https://kubernetes.io/) + [Qinglong](https://github.com/whyour/qinglong) + [Longhorn](https://longhorn.io/)

## Pre-requisites

- Install Longhorn, Ref: [K8s PostgreSQL Longhorn](https://github.com/jerryshell/k8s-postgres-longhorn)
- TLS Ingress, Ref: [K8s Traefik cert-manager DNS01 TLS](https://github.com/jerryshell/k8s-traefik-cert-manager-dns01-tls)

## Git clone

```bash
git clone https://github.com/jerryshell/k8s-qinglong-longhorn.git
cd k8s-qinglong-longhorn
```

## PVC + Deployment + Service

```bash
kubectl apply -f k8s/
```

## Ingress

Replace `qinglong.jerryshell.eu.org` with your own domain

```bash
export HOST=qinglong.jerryshell.eu.org
cat k8s/ingress/ingress.yaml | envsubst | kubectl apply -f -
```

## TLS Ingress

Replace `qinglong.jerryshell.eu.org` with your own domain

```bash
export HOST=qinglong.jerryshell.eu.org
cat k8s/ingress/tls-ingress.yaml | envsubst | kubectl apply -f -
```

## Delete

```bash
kubectl delete --ignore-not-found=true -f k8s/ -f k8s/ingress/
```

## LICENSE

[GNU Affero General Public License v3.0](https://choosealicense.com/licenses/agpl-3.0/)
