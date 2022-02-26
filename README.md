# FUJITSU Enterprise Postgres Operator for Kubernetes Helm Chart

FUJITSU Enterprise Postgres delivers an enterprise-grade PostgreSQL in Kubernetes and OpenShift Container Platform. This solution provides the flexibility of a hybrid cloud solution with operational simplicity, while delivering an enhanced distribution of PostgreSQL to support enterprise-level workloads and provide improved deployment and management, availability, performance, data governance and security. Available as a multi-architecture container built for both amd64 and s390x.

The download and Use of the Product is strictly subject to the terms of the End User License Agreement with Fujitsu Limited found at https://www.fast.fujitsu.com/fujitsu-enterprise-postgres-license-agreements. Where the Product that has been embedded as a whole or part into a third party program, only Authorised Customers may download and use the Product.


## Supported platforms

Depending on the version of the FUJITSU Enterprise Postgres Operator, it supports the following platforms:

| Helm Chart version    | Kubernetes | OpenShift Container Platform | Architecture          |
|-----------------------|------------|------------------------------|-----------------------|
| v1.1.0                | 1.19+      | 4.6 - 4.9                    | amd64, s390x, ppc64le |
| v1.0.0                | 1.19+      | 4.6 - 4.9                    | amd64, s390x          |

## Quick Start

The FUJITSU Enterprise Postgres Operator can be installed in any namespace to manage the lifecycle of a Postgres cluster using FUJITSU Enterprise Postgres Server within that namespace. It holds the operator deployment and all dependent
objects like permissions, custom resources and corresponding StatefulSets.

### Installation

To create the namespace and deploy the operator, run the following commands

```sh
$ kubectl create namespace fep
$ helm repo add fep https://fujitsu.github.io/fep-operator-helm
$ helm repo update 
$ helm install fep-operator fep/fujitsu-enterprise-postgres-operator -n fep
```

These commands deploy FUJITSU Enterprise Postgres Operator on the Kubernetes cluster.


## Uninstalling the Chart

To uninstall/delete the `fep-operator-release` deployment:

```sh
$ helm uninstall fep-operator
```

The command removes all the Kubernetes components associated with the chart and deletes the release.