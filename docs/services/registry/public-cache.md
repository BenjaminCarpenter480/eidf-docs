# The Library and Public Caches

ECIR provides a common library of standard images. ECIR will also provide cache projects for three major registries which allow images to be stored for 7 days after use in ECIR for convenient access.

## The Library

The Library is a public project containing ECIR copies of commonly used container images on the GPU Service. This will be updated over time to reflect use and updates on the service.

To use an image from the Library, the image name should be preceded by registry.eidf.ac.uk/library, for example if an Ubuntu image with the tag latest were available in the Library it would be:

```bash
registry.eidf.ac.uk/library/ubuntu:latest
```

Use of images from the Library will not count towards project image storage on the ECIR.

The Library will be updated as images are deprecated or updated and is read only for project users.

Users can use public registries to download images, the ECIR is in place to try to reduce request load on public systems.

Users can submit images to be added to the Library where they have built images they think would be useful for other users.

## Public Caches

Three main public registries are routed through proxy caches on ECIR. The proxy cache means that a user can pull a public image from a public registry and the ECIR will store a copy of that image. Images in the cache which are pulled in a 7 day period will be retained, otherwise images unused for 7 days will be removed from the cache.

This is to reduce pressure on public registries from EIDF systems and to reduce the chance of the public services rate limiting.

The three services which have cache projects are:

* Dockerhub [https://hub.docker.com](https://hub.docker.com) - Project docker-cache
* GHCR [https://ghcr.io](https://ghcr.io) - Project ghcr-cache
* NVCR [https://nvcr.io](https://nvcr.io) - Project nvcr-cache

To use a cache project, the ECIR address and the project name should be pre-pending the name of the image, for example to pull the image, `nvidia/pytorch:25.05-py3` from the Nvidia (NVCR) registry, you would use:

```bash
registry.eidf.ac.uk/nvidia-cache/nvidia/pytorch:25.05-py3
```

For Docker, top level images can be referred to directly, such as:

```bash
registry.eidf.ac.uk/docker-cache/alpine:latest
```

Or if they are part of an organisation public repository:

```bash
registry.eidf.ac.uk/docker-cache/mcp/slack:latest
```
