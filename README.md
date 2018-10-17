[![CircleCI](https://circleci.com/gh/bitnami/bitnami-docker-heapster/tree/master.svg?style=shield)](https://circleci.com/gh/bitnami/bitnami-docker-heapster/tree/master)

# What is Heapster?

Heapster is an open source, feature rich metrics dashboard and graph editor for Graphite, Elasticsearch, OpenTSDB, Prometheus and InfluxDB.

[https://github.com/kubernetes/heapster](https://github.com/kubernetes/heapster)

# TL;DR;

Deploy Heapster on your [Kubernetes cluster](https://github.com/kubernetes/heapster/tree/master/docs).

# Why use Bitnami Images?

* Bitnami closely tracks upstream source changes and promptly publishes new versions of this image using our automated systems.
* With Bitnami images the latest bug fixes and features are available as soon as possible.
* Bitnami containers, virtual machines and cloud images use the same components and configuration approach - making it easy to switch between formats based on your project needs.
* Bitnami images are built on CircleCI and automatically pushed to the Docker Hub.
* All our images are based on [minideb](https://github.com/bitnami/minideb) a minimalist Debian based container image which gives you a small base container image and the familiarity of a leading linux distribution.
* Bitnami container images are released daily with the latest distribution packages available.

[![Anchore Image Overview](https://anchore.io/service/badges/image/0b0dcc375d2b957f81eeabfeb46067173366925fa9a38817cddb5c5de407ab5b)](https://anchore.io/image/dockerhub/bitnami%2Fheapster%3Alatest#security)

> The image overview badge contains a security report with all open CVEs. Click on 'Show only CVEs with fixes' to get the list of actionable security issues.

# Why use a non-root container?

Non-root container images add an extra layer of security and are generally recommended for production environments. However, because they run as a non-root user, privileged tasks are typically off-limits. Learn more about non-root containers [in our docs](https://docs.bitnami.com/containers/how-to/work-with-non-root-containers/).

# Supported tags and respective `Dockerfile` links

> NOTE: Debian 8 images have been deprecated in favor of Debian 9 images. Bitnami will not longer publish new Docker images based on Debian 8.

Learn more about the Bitnami tagging policy and the difference between rolling tags and immutable tags [in our documentation page](https://docs.bitnami.com/containers/how-to/understand-rolling-tags-containers/).


* [`1-ol-7`, `1.5.4-ol-7-r76` (1/ol-7/Dockerfile)](https://github.com/bitnami/bitnami-docker-heapster/blob/1.5.4-ol-7-r76/1/ol-7/Dockerfile)
* [`1-debian-9`, `1.5.4-debian-9-r74`, `1`, `1.5.4`, `1.5.4-r74`, `latest` (1/debian-9/Dockerfile)](https://github.com/bitnami/bitnami-docker-heapster/blob/1.5.4-debian-9-r74/1/debian-9/Dockerfile)

Subscribe to project updates by watching the [bitnami/heapster GitHub repo](https://github.com/bitnami/bitnami-docker-heapster).

# Get this image

The recommended way to get the Bitnami Heapster Docker Image is to pull the prebuilt image from the [Docker Hub Registry](https://hub.docker.com/r/bitnami/heapster).

```bash
$ docker pull bitnami/heapster:latest
```

To use a specific version, you can pull a versioned tag. You can view the [list of available versions](https://hub.docker.com/r/bitnami/heapster/tags/) in the Docker Hub Registry.

```bash
$ docker pull bitnami/heapster:[TAG]
```

If you wish, you can also build the image yourself.

```bash
$ docker build -t bitnami/heapster:latest https://github.com/bitnami/bitnami-docker-heapster.git
```

# Contributing

We'd love for you to contribute to this container. You can request new features by creating an [issue](https://github.com/bitnami/bitnami-docker-heapster/issues), or submit a [pull request](https://github.com/bitnami/bitnami-docker-heapster/pulls) with your contribution.

# Issues

If you encountered a problem running this container, you can file an [issue](https://github.com/bitnami/bitnami-docker-heapster/issues). For us to provide better support, be sure to include the following information in your issue:

- Host OS and version
- Docker version (`docker version`)
- Output of `docker info`
- Version of this container
- The command you used to run the container, and any relevant output you saw (masking any sensitive information)

# License
Copyright 2018 Bitnami

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
