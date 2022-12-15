# Faas-tasks: Optimized Resource Management for FaaS platforms

Faas-tasks is a research project whose aim is to explore resource management strategies for modern and upcoming workloads deployed on FaaS (Functions as a Service) platforms.

In particular, we are investigating scheduling strategies for single-function tasks and multi-function tasks (i.e., tasks workflow) with heterogeneous granularities and priorities.

Our ongoing work is based on the [knative](https://knative.dev/) serverless framework.
## Table of contents

#### **1. [General overview](#General-overview)**

#### **2. [Intallation](#Installation)**
        
#### **3. [Usage](#Usage)**
#### **4. [Usage](#Usage)**

#### **5. [Tests](#tests)**

## General overview

Knative is an Open Source infrastructure for building, deploying and managing serverless applications on kubernetes. 

There are two compoments:

![knativearch](knative1.drawio.png)

1. **Knative Serving**

   Ideal to running applications services inside kubernetes and the scaling of applications you plan to deploy.

   ![serving-architecture](knativeServing-architecture.png)
   
   The architecture above shows how a service is created and can be summarized as follows:
   
    - The service automatically creates a configuration and a route for the service
    - The configuration manages the revisions
    - Each revision is associated to a Kubernetes deployment

   Above the knative serving architecture. For [more details](https://knative.dev/docs/concepts/) about its components.

2. **Knative Eventing**

   Knative Eventing is a collection of APIs that enable you to use an event-driven architecture with your applications. You can use these APIs to create components that route events from event producers to event consumers, known as sinks, that receive events. Sinks can also be configured to respond to HTTP requests by sending a response event. [Sources](https://knative.dev/docs/eventing/).

Our project will focus on Knative Serving.   

## Intallation 

   In this section, we will present the different installation modes of the knative platform. 
   
   1. **Setup a Serverless (Knative) Cluster in single-node**
   
      * Requirements
        - Knative requires a Kubernetes cluster v1.21
        - Hardware support for virtualization and KVM
        - Have docker for vm driver 
        - The Kubernetes CLI to run commands against Kubernetes clusters
        - The Knative CLI kn
        - we use Ubuntu 20.04 LTS
        - You need to have a minimum of 3 CPUs, 10 GB of SSD  and 3 GB of RAM available for the cluster to be created
        
   The following table presents the different hardware and software characteristics used in our work.
       
   |Informations matériels et logiciels| Descriptions |
   |-----------------------------------|--------------| 
   |computer brand                     |Dell-Precision-3561|
   |Ram memory                       | 16 GB|
   |Processor                    | 11th Gen Intel® Core™ i7-11850H @ 2.50GHz × 16|
   |Storage                      | 512,1 GB SSD|
   |OS name       | Ubuntu 20.04.5 LTS|
   |OS type        | 64 bits|

