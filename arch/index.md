---
layout: default
title: Architecture
nav_order: 3
has_children: true
---

# OLM v1 Architecture

The user experience captured in the OLM V1 PRD introduces many requirements that are best satisfied by a microservices architecture. The OLM V1 experience currently relies on four projects:
- [The Operator-Controller project](https://github.com/operator-framework/operator-controller/), which is the top level component allowing users to specify operators they'd like to install.
- [The Catalogd project](https://github.com/operator-framework/catalogd/), which hosts operator content and helps users discover installable content.
- [The Deppy project](https://github.com/operator-framework/deppy/), which enables the operator-controller to identify valid installs and upgrades from the list of installable content provided via the Catalogd project.
- [The RukPak project](https://github.com/operator-framework/rukpak/), which facilitates the installation of operators.

Each of the projects listed above have their own governance, release milestones, and release cadence. However, from a technical perspective, the "OLM V1 experience" matches the experienced offered by the operator-controller project, the top level component which introduces dependencies on RukPak, Deppy, and the Catalogd projects.

