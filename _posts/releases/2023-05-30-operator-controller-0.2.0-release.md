---
layout: post
title: Operator Controller v0.2.0 released!
tags: operator-controller
---
# Operator Controller v0.2.0

## Installation

```sh
curl -L -s https://github.com/operator-framework/operator-controller/releases/download/v0.2.0/install.sh | bash -s
```

### What's Changed

* Update RELEASE.md to point to correct url by @awgreene in #212
* Fail early on e2e setup failure by @jmprusi in #214
* Adds new Status condition "Resolved" and related status field "resolvedBundleResource" to Operator CR by @jmprusi in #213
* Makefile: don't globally export GOOS=linux by @joelanford in #221
* Remove TypeReady Condition by @tmshort in #217
* Operator CR Installed status condition by @jmprusi in #218
* Clean-up of operator conditions with helper funcs by @jmprusi in #228
* Fix README.md by @tmshort in #225
* Removes util package by @m1kola in #223
* Moves ./controllers into ./internal and ./main.go into ./cmd by @m1kola in #222
* Define default logs container for operator-controller pod by @joelanford in #240
* bump catalogd to v0.2.0 by @joelanford in #241
