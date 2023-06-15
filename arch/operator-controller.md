---
title: Operator Controller
layout: default
parent: Architecture
nav_order: 1
---

# Operator Controller

The operator-controller is the central component of Operator Lifecycle Manager (OLM) v1. It extends Kubernetes with an API through which users can install Operators.

## Description
OLM v1 is the follow-up to OLM v0, located [here](https://github.com/operator-framework/operator-lifecycle-manager). It consists of four different components, including this one, which are as follows:
* operator-controller
* [deppy](https://github.com/operator-framework/deppy)
* [rukpak](https://github.com/operator-framework/rukpak)
* [catalogd](https://github.com/operator-framework/catalogd)

## Getting Started
You’ll need a Kubernetes cluster to run against. You can use [KIND](https://sigs.k8s.io/kind) to get a local cluster for testing, or run against a remote cluster.
**Note:** Your controller will automatically use the current context in your kubeconfig file (i.e. whatever cluster `kubectl cluster-info` shows).

### Running on the cluster
1. Install Instances of Custom Resources:

```sh
kubectl apply -f config/samples/
```

2. Build and push your image to the location specified by `IMG`:
	
```sh
make docker-build docker-push IMG=<some-registry>/operator-controller:tag
```
