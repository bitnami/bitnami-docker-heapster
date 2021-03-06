
# Deprecation notice

Heapster project is deprecated. Consider using [metrics-server](https://github.com/bitnami/bitnami-docker-metrics-server). The container images will continue being available in Docker Hub and this repository will be archived in 30 days.

# What is Heapster?

Heapster is an open source, feature rich metrics dashboard and graph editor for Graphite, Elasticsearch, OpenTSDB, Prometheus and InfluxDB.

[https://github.com/kubernetes/heapster](https://github.com/kubernetes/heapster)

# TL;DR;

Deploy Heapster on your [Kubernetes cluster](https://github.com/kubernetes/heapster/tree/master/docs).

# How to deploy Heapster in Kubernetes?

> NOTE: If you are pulling from a private containers registry, replace the image name with the full URL to the docker image. E.g.
> 
> ```
> --image='your-registry/heapster:your-version'
> ```

To run heapster run the following comand:

> kubectl run heapster --image=bitnami/heapster -- --source=kubernetes

You will need to set some configuration in your kubernetes cluster. Read more about this configuration steps in the [heapster's source configuration documentation](https://github.com/kubernetes/heapster/blob/master/docs/source-configuration.md).

# Why use Bitnami Images?

* Bitnami closely tracks upstream source changes and promptly publishes new versions of this image using our automated systems.
* With Bitnami images the latest bug fixes and features are available as soon as possible.
* Bitnami containers, virtual machines and cloud images use the same components and configuration approach - making it easy to switch between formats based on your project needs.
* All our images are based on [minideb](https://github.com/bitnami/minideb) a minimalist Debian based container image which gives you a small base container image and the familiarity of a leading linux distribution.
* Bitnami container images are released daily with the latest distribution packages available.


> This [CVE scan report](https://quay.io/repository/bitnami/heapster?tab=tags) contains a security report with all open CVEs. To get the list of actionable security issues, find the "latest" tag, click the vulnerability report link under the corresponding "Security scan" field and then select the "Only show fixable" filter on the next page.

# Why use a non-root container?

Non-root container images add an extra layer of security and are generally recommended for production environments. However, because they run as a non-root user, privileged tasks are typically off-limits. Learn more about non-root containers [in our docs](https://docs.bitnami.com/containers/how-to/work-with-non-root-containers/).

# Supported tags and respective `Dockerfile` links

> NOTE: Debian 8 images have been deprecated in favor of Debian 9 images. Bitnami will not longer publish new Docker images based on Debian 8.

Learn more about the Bitnami tagging policy and the difference between rolling tags and immutable tags [in our documentation page](https://docs.bitnami.com/containers/how-to/understand-rolling-tags-containers/).


* [`1-debian-9`, `1.5.4-debian-9-r191`, `1`, `1.5.4`, `1.5.4-r191`, `latest` (1/debian-9/Dockerfile)](https://github.com/bitnami/bitnami-docker-heapster/blob/1.5.4-debian-9-r191/1/debian-9/Dockerfile)

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
