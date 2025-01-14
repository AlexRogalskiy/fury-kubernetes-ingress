# Fury Kubernetes Ingress

This repo contains Ingress Controller and TLS certificate management components you need to manage external access to
your services in your cluster.

## Ingress Packages

The following packages are included in Fury Kubernetes Ingress katalog:

- [cert-manager](katalog/cert-manager): cert-manager is a Kubernetes
add-on to automate the management and issuance of TLS certificates
from various issuing sources. Version: **v1.6.1**
- [forecastle](katalog/forecastle): Forecastle gives you access to a control
panel where you can see your running applications and access them
on Kubernetes. Version: **1.0.70**.
- [nginx](katalog/nginx): The NGINX Ingress Controller for Kubernetes
provides delivery services for Kubernetes applications. Version: **1.1.0**
- [dual-nginx](katalog/dual-nginx): It deploys two identical NGINX ingress controllers
but with two different scopes: public/external and private/internal.  Version: **1.1.0**
- [nginx-ldap-auth](katalog/nginx-ldap-auth): Use this to provide an ingress authentication over LDAP for
Kubernetes. Version: **1.0.6**
- [pomerium](katalog/pomerium): Use this to provide ingress authentication over dex oidc auth. Version **0.15.8**

## Compatibility

| Module Version / Kubernetes Version | 1.14.X             | 1.15.X             | 1.16.X             | 1.17.X             | 1.18.X             | 1.19.X             | 1.20.X             | 1.21.X             | 1.22.X    | 1.23.X    |
|-------------------------------------|:------------------:|:------------------:|:------------------:|:------------------:|:------------------:|:------------------:|:------------------:|:------------------:|:---------:|-----------|
| v1.1.0                              |                    |                    |                    |                    |                    |                    |                    |                    |           |           |
| v1.2.0                              | :white_check_mark: | :white_check_mark: | :white_check_mark: |                    |                    |                    |                    |                    |           |           |
| v1.3.0                              | :white_check_mark: | :white_check_mark: | :white_check_mark: |                    |                    |                    |                    |                    |           |           |
| v1.4.0                              | :white_check_mark: | :white_check_mark: | :white_check_mark: |                    |                    |                    |                    |                    |           |           |
| v1.5.0                              | :white_check_mark: | :white_check_mark: | :white_check_mark: |                    |                    |                    |                    |                    |           |           |
| v1.6.0                              | :white_check_mark: | :white_check_mark: | :white_check_mark: |                    |                    |                    |                    |                    |           |           |
| v1.6.1                              | :white_check_mark: | :white_check_mark: | :white_check_mark: |                    |                    |                    |                    |                    |           |           |
| v1.7.0                              |                    |                    | :white_check_mark: | :white_check_mark: | :white_check_mark: |                    |                    |                    |           |           |
| v1.8.0                              |                    |                    | :white_check_mark: | :white_check_mark: | :white_check_mark: | :warning:          |                    |                    |           |           |
| v1.8.1                              |                    |                    | :white_check_mark: | :white_check_mark: | :white_check_mark: | :warning:          |                    |                    |           |           |
| v1.8.2                              |                    |                    | :white_check_mark: | :white_check_mark: | :white_check_mark: | :warning:          |                    |                    |           |           |
| v1.9.0                              |                    |                    |                    | :warning:          | :warning:          | :warning:          | :warning:          | :warning:          |           |           |
| v1.9.1                              |                    |                    |                    | :white_check_mark: | :white_check_mark: | :white_check_mark: | :warning:          | :warning:          |           |           |
| v1.10.0                             |                    |                    |                    |                    | :white_check_mark: | :white_check_mark: | :white_check_mark: | :warning:          |           |           |
| v1.11.0                             |                    |                    |                    |                    |                    | :white_check_mark: | :white_check_mark: | :white_check_mark: | :warning: |           |
| v1.11.1                             |                    |                    |                    |                    |                    | :white_check_mark: | :white_check_mark: | :white_check_mark: | :warning: |           |
| v1.11.2                             |                    |                    |                    |                    |                    | :white_check_mark: | :white_check_mark: | :white_check_mark: | :warning: |           |
| v1.12.0                             |                    |                    |                    |                    |                    |                    | :white_check_mark: | :white_check_mark: | :warning: | :warning: |

- :white_check_mark: Compatible
- :warning: Has issues
- :x: Incompatible

### Warning

- :warning: : module version: `v1.9.0` and Kubernetes Version: `1.20.x`. It works as expected. Marked as a warning
because it is not officially supported by [SIGHUP](https://sighup.io).
- :warning: : module version: `v1.9.0`. Has some problems exposing metrics and with the log recollection.
Move to v1.9.1 instead. [Follow the migration path.](docs/releases/v1.9.1.md)
- :warning: : module version: `v1.10.0` and Kubernetes Version: `1.21.x`. It works as expected. Marked as a warning
because it is not officially supported by [SIGHUP](https://sighup.io).
- :warning: : module version: `v1.11.X` and Kubernetes Version: `1.22.x`. This version is not fully supported since the component
  `forecastle` is not supported in k8s version `1.22`
- :warning: : module version: `v1.12.0` and Kubernetes Version: `1.23.x`. This version is not fully supported since the component
  `forecastle` is not supported in k8s version `1.23`

## Development

To read about testing, tagging, linting, etc. of `fury-kubernetes-ingress` module,
refer the [contribution guidelines](docs/CONTRIBUTING.md).

## LICENSE

For license details, please see [LICENSE](LICENSE)
