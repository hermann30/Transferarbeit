### Install Helm Package Manager

https://helm.sh/docs/intro/install/

### Add Bitnami Repo for helm charts

```bash
# Add Bitnami Repo for helm
helm repo add bitnami https://charts.bitnami.com/bitnami
helm repo update
```

### Install NGINX Ingress

https://github.com/bitnami/charts/tree/main/bitnami/nginx-ingress-controller

```bash
# Install nginx-ingress
helm upgrade --install nginx-ingress bitnami/nginx-ingress-controller --namespace nginx-ingress --create-namespace
```

#### Install Kube-Prometheus

https://github.com/bitnami/charts/tree/main/bitnami/kube-prometheus

```bash
# Install kube-prometheus
helm upgrade --install kube-prometheus bitnami/kube-prometheus --namespace kube-prometheus --create-namespace -f kube-prometheus/values.yml
```

#### Install Grafana

https://github.com/bitnami/charts/tree/main/bitnami/grafana

```bash
# Install grafana
helm upgrade --install grafana bitnami/grafana --namespace grafana --create-namespace -f grafana/values.yml
```
