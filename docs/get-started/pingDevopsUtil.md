---
title: The ping-devops Utility
---
# The `ping-devops` Utility

`ping-devops` is our general DevOps command-line utility.

## Dependent Utilities

To perform all of its operations, `ping-devops` has a dependency on the following utilities:

* openssl
* base64
* kustomize
* kubectl
* envsubst
* jq

## Installation and Upgrades

Use Homebrew to install `ping-devops` on MacOS or Linux.

1. To install, enter:

    ```sh
    brew tap pingidentity/devops
    brew install ping-devops
    ```

1. To upgrade, enter:

    ```sh
    brew upgrade ping-devops
    ```

1. To check for upgrades, run the following command.

    !!! note "Check regularly"
        Check for upgrades regularly.

    ```sh
    ping-devops version
    ```

    The dependent utilities for `ping-devops` are also installed or upgraded during this process.

1. On Linux systems, install or upgrade the `ping-devops` utility and `bash_profile` aliases to your current directory by entering:

    ```sh
    curl -sL https://bit.ly/ping-devops-install | bash
    ```

    Follow instructions to copy to your preferred location.

    Ensure you have the dependent utilities for `ping-devops` installed as well.

## `ping-devops` Usage

Enter `ping-devops` in a terminal to display the commands listing, which is shown in the following example.

```sh
#####################################################################
#  Ping Identity DevOps (version 0.7.2)
#
#  Documentation: https://devops.pingidentity.com
#   GitHub Repos: https://github.com/topics/ping-devops
#####################################################################

General Usage:
  ping-devops config
  ping-devops info [-v]
  ping-devops version
  ping-devops clean
  ping-devops topic [ {topic-name} ]

Generate Kubernetes/Kustomize/License Resources:
  ping-devops generate devops-secret
  ping-devops generate tls-secret {domain}
  ping-devops generate ssh-id-secret {ssh id_rsa file}
  ping-devops generate license {product} {ver}
  ping-devops generate license-secret {license file}
  ping-devops generate license-secret {product} {ver}
  ping-devops generate kustomization.yaml

Running Docker/Kubernetes Environments:
  ping-devops docker     [info|start|stop|rm|clean]
  ping-devops kubernetes [info|start|rm|clean]

Hashicorp Vault:
  ping-devops vault get-token
  ping-devops vault create-annotations {secret}

Further help:
  https://github.com/pingidentity/ping-devops
```
