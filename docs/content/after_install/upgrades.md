+++
title = "Upgrades"
date = 2022-02-09T17:56:26+01:00
weight = 1
pre = "<b>- </b>"
+++

## Kubernetes

Upgrades can be triggered from Kubernetes with `system-upgrade-controller` installed in your cluster. [See the cOS documentation](https://rancher-sandbox.github.io/cos-toolkit-docs/docs/getting-started/upgrading/#integration-with-system-upgrade-controller)

## Manual

### Upgrade to latest

Upgrades can be triggered manually as well from the nodes.

To upgrade to latest available version, run `c3os upgrade`. 

To specify a version, run `c3os upgrade <version>`. Use `--force` to force upgrading to avoid checking versions. All the available versions can be list with: `c3os upgrade list-releases`.

It is possible altough to use the same commandset from `cOS`. So for example, the following works too:

```
cos-upgrade --no-verify --docker-image quay.io/c3os/c3os:opensuse-v1.21.4-22
```

c3os images are released on [quay.io](https://quay.io/repository/c3os/c3os).

[See also the general cOS documentation](https://rancher-sandbox.github.io/cos-toolkit-docs/docs/getting-started/upgrading/#upgrade-to-a-specific-container-image) which applies for `c3os` as well.