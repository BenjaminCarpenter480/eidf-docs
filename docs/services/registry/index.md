# Overview

EIDF Container Image Registry (ECIR) is an image registry for use in EIDF and related services. ECIR is a [Harbor](https://goharbor.io) installation providing services for image storage, vulnerability scanning and Software Bill of Materials (SBOM) generation.

## Projects on ECIR

ECIR provides projects with a private space on the service where a project can host multiple container image repositories. For information on what projects get with an ECIR private space, see [ECIR project space](./projects.md)

## Public Cache on ECIR

ECIR hosts public cache projects for commonly used images. If you use an image which is commonly pulled from public repositories, using a cache copy can reduce the impact on public services. For information on the current public caches, see [Public Caches](./public-cache.md)

## Working with ECIR

For more information on how to work with ECIR, refer to [Working with ECIR](./working-with.md).

## Features

### Vulnerability scanning by Trivy

All images in the ECIR will be scanned by [Trivy](https://trivy.dev/latest/) by default. A vulnerability report will be available shortly after push to the repositories for all new or updated images.

The report will highlight fixable known issues.

!!! important "Not Foolproof"

    Just because Trivy indicates few or no vulnerabilities this does not mean the scanned image is free of security issues, Trivy can only scan for known issues and specific types of security problems.

Projects can request that images with vulnerabilities about a set level cannot be deployed from the ECIR.

### Software Bill of Materials (SBOM)

SBOMs will be automatically generated on push to the ECIR and associated with an image. This will list what is in an image with its version and license information where possible.
