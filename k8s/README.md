# Kubernetes deployments

## Online Boutique
`helm upgrade --intsall onlineboutique oci://us-docker.pkg.dev/online-boutique-ci/charts/onlineboutique --version 0.10.7 -n boutique --create-namespace -f k8s/boutique-values.yaml`

## Monitoring
`helm upgrade --install monitoring prometheus-community/kube-prometheus-stack --version 92.10.1 -n monitoring --create-namespace -f k8s/monitoring-values.yaml`

## Chaos Mesh
`helm upgrade --install chaos-mesh chaos-mesh/chaos-mesh --version 2.8.7 -n chaos-mesh --create-namespace -f k8s/chaos-mesh-values.yaml`

Opt the target namespace in (required because enableFilterNamespace is on):
`kubectl annotate namespace boutique chaos-mesh.org/inject=enabled`
