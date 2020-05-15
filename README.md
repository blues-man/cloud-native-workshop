# Cloud Native Workshop

[![Contribute](factory-contribute.svg)](https://codeready-workspaces.apps.cluster-nantes-715e.nantes-715e.example.opentlc.com/factory?url=https://github.com/blues-man/cloud-native-workshop/tree/demo)


## Overview

This one day hands-on cloud-native workshops provides developers and introduction to cloud-natives applications
and gives them an experience of building cloud-native applications using OpenShift, Eclipse Che7, Spring Boot,
Quarkus, Vert.x and more.


![Architecture](https://raw.githubusercontent.com/blues-man/cloud-native-workshop/3.2/guide/images/coolstore-arch.png "Architecture")

![Architecture Screenshot](https://raw.githubusercontent.com/jbossdemocentral/coolstore-microservice/ocp-4.1/docs/images/store.png "CoolStore Online Shop")

## Agenda

* Introduction to Cloud-Native Development
* Getting your Developer Workspace with Eclipse Che7
* Building Services with Quarkus
* Building Services with Spring Boot
* Building Reactive Services with Vert.x
* Monitoring Application Health
* Service Resilience and Fault Tolerance
* Externalize Application Configuration
* Building Cloud-Native Pipelines with Tekton
* Connecting and monitoring microservice applications with Service Mesh
* Setting up A/B Testing with Service Mesh

## Deploy the Workshop on RHPDS

An [Operator](https://docs.openshift.com/container-platform/4.2/operators/olm-what-operators-are.html)
is provided for deploying the workshop infrastructure (lab instructions, Nexus, Gogs, Eclipse Che, etc)
on OpenShift.

Please follow the instructions from [OpenShift Workshop Operator](https://github.com/mcouliba/openshift-workshop-operator)
and deploy the following **Workshop** custom resource [cloud_native_workshop_cr.yaml](https://github.com/mcouliba/openshift-workshop-operator/blob/master/deploy/crds/cloud_native_workshop_cr.yaml)

## Run locally the lab instructions

In order to run the guide locally, please follow the instructions below:

```
$ git clone
$ cd cloud-native-workshop/guide
$ docker run -it --rm -p 8080:8080 \
      -v $(pwd):/app-data \
      -e LOG_TO_STDOUT#true \
      -e CONTENT_URL_PREFIX#"file:///app-data" \
      -e WORKSHOPS_URLS#"file:///app-data/_workshop.yml" \
      quay.io/osevg/workshopper:latest
```
