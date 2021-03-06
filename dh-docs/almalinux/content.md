# AlmaLinux OS

[**`AlmaLinux OS`**](https://almalinux.org/) is an Open Source and forever-free enterprise Linux distribution, governed and driven by the community, focused on long-term stability and a robust production-grade platform. AlmaLinux OS is 1:1 binary compatible with RHEL® 8 and it was founded by the team behind the well-established [**`CloudLinux OS`**](https://www.cloudlinux.com/all-products/product-overview/cloudlinuxos).

%%LOGO%%

## About this image

[AlmaLinux OS](https://almalinux.org/) images can be use with all [OCI complaint](https://opencontainers.org/) container runtime environments like Docker, Podman and Kubernetes and serve as drop-in replacemenets for `centos` images as it reaches [End of Life](https://centos.org/centos-linux-eol/).

### Platform image, `latest` tag

The default (platform) image is a general-purpose image with a full DNF stack and basic tools like bintools, find, tar, minimal-vim, etc.

The `%%IMAGE%%:latest` tag will always point to the latest stable release of the default image. Major releases and minor releases are also tagged with their version (e.g. `%%IMAGE%%:8` or `%%IMAGE%%:8.4`).

### Minimal image, `minimal` tag

The minimal image is a stripped-down image that uses the [**`microdnf`**](https://github.com/rpm-software-management/microdnf) as package manager which uses `libdnf` and hence doesn't require Python. This image is `52%` smaller in size (`37MB` download, `102MB` expanded), contains a very limited package set. It is designed for applications that come with their own dependencies bundled (e.g. GO, NodeJS, Java).

The `%%IMAGE%%:minimal` tag always points to the most recent version of the minimal image. Tags for major (e.g. `%%IMAGE%%:8-minimal`) and minor (e.g. `%%IMAGE%%:8.4-minimal`) releases are also available.

### Upgrade policy

All images for supported releases will be updated monthly or as needed for security fixes.

### How It's Made

The rootfs tarballs for this image are built using the [livemedia-creator tool](http://weldr.io/lorax/livemedia-creator.html). The build script and kickstart files are available in the [AlmaLinux/docker-images](https://github.com/AlmaLinux/docker-images) git repository.

### Other variant images

AlmaLinux OS now offers new variant of images [**`almalinux/8-base`**](https://hub.docker.com/r/almalinux/8-base), [**`almalinux/8-init`**](https://hub.docker.com/r/almalinux/8-init), [**`almalinux/8-micro`**](https://hub.docker.com/r/almalinux/8-micro) and [**`almalinux/8-minimal`**](https://hub.docker.com/r/almalinux/8-minimal)  to be aligned with  RedHat UBI images.
