# Azure Service Operator Demo

This repo contains demo code for Azure Service Operator with FluxCD.

## Installation

``` bash
kubectl create ns flux

fluxctl install --git-url 'git@github.com:nmeisenzahl/aso-fluxcd-sample.git' \
  --git-path workloads \
  --git-branch master \
  --git-readonly \
  --git-email 'mail@domain.com' \
  --namespace flux | kubectl apply -f -

fluxctl identity --k8s-fwd-ns flux
```
