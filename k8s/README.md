# Kubernetes deployments

## Online Boutique
`helm upgrade --intsall onlineboutique oci://us-docker.pkg.dev/online-boutique-ci/charts/onlineboutique --version 0.10.7 -n boutique --create-namespace -f k8s/boutique-values.yaml`

## Monitoring
`helm upgrade --install monitoring prometheus-community/kube-prometheus-stack --version 92.10.1 -n monitoring --create-namespace -f k8s/monitoring-values.yaml`