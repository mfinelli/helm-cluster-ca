# helm-cluster-ca

A helm chart to create a cluster-internal private certificate authority using
[cert-manager](https://cert-manager.io).

This is essentially just packaging the example provided upstream
https://cert-manager.io/docs/configuration/selfsigned/#bootstrapping-ca-issuers
in order to make it easily reusable across clusters.

Obviously, there is a dependency on `cert-manager` and its CRDs, but you must
install it separately, beforehand as it's not listed as a dependency of this
chart.

## usage

```shell
helm repo add mfinelli https://charts.finelli.dev
helm install --namespace cert-manager mfinelli/cluster-ca
```

## license

```
Copyright 2022 Mario Finelli

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
