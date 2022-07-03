---
title: faasd
date: 2021-02-20T23:27:49.354-08:00
tags:
  - serverless
git: https://github.com/openfaas/faasd
---
faasd is part of [[OpenFaaS]]. I got it mostly up and running on [[Digital Ocean]], using the [cloud-init setup article](https://blog.alexellis.io/deploy-serverless-faasd-with-cloud-init/).

> faasd is OpenFaaS reimagined, but without the cost and complexity of Kubernetes. It runs on a single host with very modest requirements, making it fast and easy to manage. Under the hood it uses containerd and Container Networking Interface (CNI) along with the same core OpenFaaS components from the main project.

Continued from the [Github README](https://github.com/openfaas/faasd): 

* faasd is a static Golang binary
* uses the same core components and ecosystem of OpenFaaS
* uses containerd for its runtime and CNI for networking
* is multi-arch, so works on Intel x86_64 and ARM out the box
* can run almost any other stateful container through its docker-compose.yaml file

You can [Deploy faasd to your Raspberry Pi](https://blog.alexellis.io/faasd-for-lightweight-serverless/).