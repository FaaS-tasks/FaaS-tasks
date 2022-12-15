# Faas-tasks: Optimized Resource Management for FaaS platforms

Faas-tasks is a research project whose aim is to explore resource management strategies for modern and upcoming workloads deployed on FaaS (Functions as a Service) platforms.

In particular, we are investigating scheduling strategies for single-function tasks and multi-function tasks (i.e., tasks workflow) with heterogeneous granularities and priorities.

Our ongoing work is based on the [knative](https://knative.dev/) serverless framework.

## Table of contents

#### **1. [General overview](#General-overview)**

#### **2. [Intallation and usage](#installation-and-usage)**
        
1. **[Intallation](#installation)**
2. **[Usages](#usages)**

#### **3. [Tests](#tests)**

## General overview

Knative is an Open Source infrastructure for building, deploying and managing serverless applications on kubernetes. 

There are two compoments:

![knativearch](images/knative1.drawio.png)

1. **Knative Serving**

   Ideal to running applications services inside kubernetes and the scaling of applications you plan to deploy.

   ![serving-architecture](images/knativeServing-architecture.png)

   Above the knative serving architecture. For [more details](https://knative.dev/docs/concepts/) about its components.

2. **Knative Eventing**

   Knative Eventing is a collection of APIs that enable you to use an event-driven architecture with your applications. You can use these APIs to create components that route events from event producers to event consumers, known as sinks, that receive events. Sinks can also be configured to respond to HTTP requests by sending a response event. [Sources](https://knative.dev/docs/eventing/).

Our project will focus on Knative Serving.   