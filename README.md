# helm-cluster-ca

A helm chart to create a cluster-internal private certificate authority using
[cert-manager](https://cert-manager.io).

This is essentially just packaging the example provided upstream
https://cert-manager.io/docs/configuration/selfsigned/#bootstrapping-ca-issuers
in order to make it easily reusable across clusters.

Obviously, there is a dependency on `cert-manager` and its CRDs, but you must
install it separately, beforehand as it's not listed as a dependency of this
chart.
