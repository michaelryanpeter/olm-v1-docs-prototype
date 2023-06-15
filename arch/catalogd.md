---
title: Catalogd
layout: default
parent: Architecture
nav_order: 2
---

# Catalogd

Catalogd is a Kubernetes extension that unpacks [file-based catalog (FBC)](https://olm.operatorframework.io/docs/reference/file-based-catalogs/#docs) content for on-cluster APIs. As component of the Operator Lifecycle Manager (OLM) v1 microservices architecture, catalogd hosts Operators and controllers that extend Kubernetes APIs and helps customers discover installable content.

## OLM v1 ecosystem
[Describe OLM v1 at a high level]
[Link to PRD]
[Link to Milestones]

### OLM v1 components

[List and describe OLM v1 components]

## Quick start

**NOTE:** Procedure steps marked with an astericks (`*`) are likely to change in future API changes.

1. To install catalogd, perform one of the following actions:
    - Install the operator-controller, which includes catalogd, by entering the following command:
        ```sh
        $ curl -L -s https://github.com/operator-framework/operator-controller/releases/download/v0.2.0/install.sh | bash -s
        ```
    - To install catalogd, without installing the operator-controller, follow the install instructions included in the latest release[link] of catalogd.

1. Create a `Catalog` object that points to the OperatorHub Community catalog by running the following command:

    ```sh
    $ kubectl apply -f - << EOF
    apiVersion: catalogd.operatorframework.io/v1alpha1
    kind: Catalog
    metadata:
      name: operatorhubio
    spec:
      source:
        type: image
        image:
          ref: quay.io/operatorhubio/catalog:latest
    EOF
    ```

1. Verify the `Catalog` object was created successfully by running the following command:

    ```sh
    $ kubectl describe catalog/operatorhubio
    ```

1. Run the following command to get a list of packages: `*`

    ```sh
    $ kubectl get packages
    ```

1. Run the following command to get a list of bundles: `*`
