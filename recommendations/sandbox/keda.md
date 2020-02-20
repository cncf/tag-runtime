# CNCF SIG Sandbox Project Request - KEDA

## Acceptance to CNCF Sandbox

**Authors:** Jeff Hollan (@jeffhollan), Tom Kerkhove (@TomKerkhove), Anirudh Garg (@anirudhgarg)

## Background

**_Link to TOC PR_**

https://github.com/cncf/toc/issues/335

**_Link to Presentation_**

Recording: Feb 20 SIG-Runtime meeting

Slides: https://docs.google.com/presentation/d/11MssWPEyolaZwmJfg7sKE2BwSnGsmrXR3tdCscwf-WA/edit?usp=sharing

**_Link to GitHub project_**

http://github.com/kedacore/keda

## Project Goal

Deploying applications on Kubernetes has become trivial, but that's only where it begins. As a platform gains more momentum, it has to survive and adapt - Autoscaling is an important aspect to accomplish this.

While Kubernetes provides application autoscaling out-of-the-box with Horizontal Pod Autoscalers (HPA), it is sometimes too limited as it only covers resource metrics while often you want to scale on external metrics instead. In reality, that means you have to deploy 3r party metric adapters based on the system you depend on, but you can only run one in the same cluster and have to manage it.

In 2019, Kubernetes Event-driven Autoscaling (KEDA) was launched by Microsoft and Red Hat to build an open application-oriented scaling mechanism that is vendor-agnostic and acts as an external metric aggregater which allows you to use 0-to-n scaling based on a variety of external metrics for different vendors. On November 19th, 2019 KEDA v1.0 has been released which makes it production-ready and provides enterprise-grade security.

With **Kubernetes Event-driven Autoscaling (KEDA) we aim to make application autoscaling super simple**, regardless of the data source that you are using, by abstracting away the metric adapters and allowing KEDA customers to only focus on their scaling needs of their platform.

Customers can describe how their workloads, deployments or jobs, should scale based on the criteria and deploy it as a first-class resource on Kubernetes and that's it - Kubernetes Event-driven Autoscaling (KEDA) handles the rest.

**Instead of reinventing the wheel, Kubernetes Event-driven Autoscaling (KEDA) is extending Kubernetes** - When a workload has to scale from 0-to-n instances, it will automatically create an Horizontal Pod Autoscalers (HPA) until there is no work left and it gets removed again.

**Kubernetes Event-driven Autoscaling (KEDA) provides a variety of 20+ scalers which allows customers to automatically scale workloads based on external systems.** Our portfolio includes AWS, GCP, Microsoft Azure & Huawei cloud as well as other technologies such as Kafka, Prometheus, NATS and more but new scalers can be added very easily.

**By leveraging scale-to-0, Kubernetes Event-driven Autoscaling (KEDA) allows customers to build resource-friendly applications** by making the unused resouces available to other applications in the Kubernetes cluster that really need them.

**Kubernetes Event-driven Autoscaling (KEDA) provides production-grade security** by supporting pod identities, like Azure AD Pod Identity, to avoid secret management and allow for authentication re-use across multiple scalers. This allows existing deployments to run under the same minimal permissions while KEDA scalers can use higher-priviledged authentication to gain the required metrics. With this approach, we allow developers to focus on their workload while ops manages the authentication & configuration of the autoscaling, although it can be managed end-to-end by a full-stack as well.

## Current Status

__Feb 20, 2020__

- Stars: 1.8k
- Forks: 144
- Maintainers: 8 (5 Microsoft, 2 Red Hat, 1 Codit)
- Releases: [3](https://github.com/kedacore/keda/releases)
- Commits: 509
- Contributors: 50
- Integrations:
  - [Apache Kafka](https://kafka.apache.org/)
  - [AWS CloudWatch](https://aws.amazon.com/cloudwatch/)
  - [AWS Kinesis Stream](https://aws.amazon.com/kinesis/data-streams/)
  - [AWS SQS Queue](https://aws.amazon.com/sqs/)
  - [Azure Blob Storage](https://azure.microsoft.com/en-us/services/storage/blobs/)
  - [Azure Event Hubs](https://azure.microsoft.com/en-us/services/event-hubs/)
  - [Azure Monitor](https://azure.microsoft.com/en-us/services/monitor/)
  - [Azure Service Bus](https://azure.microsoft.com/en-us/services/service-bus/)
  - [Azure Storage Queue](https://azure.microsoft.com/en-us/services/storage/queues/)
  - [Google Cloud Platform Pub/Sub](https://cloud.google.com/pubsub/docs)
  - [MySQL](https://www.mysql.com/)
  - [Huawei Cloud Eye](https://www.huaweicloud.com/en-us/product/ces.html)
  - [Liiklus Topic](https://github.com/bsideup/liiklus)
  - [NATS](https://nats.io/)
  - [PostgreSQL](https://www.postgresql.org/)
  - [Prometheus](https://prometheus.io/)
  - [RabbitMQ](https://www.rabbitmq.com/)
  - [Redis](https://redis.io/)
- Adopters: 5 current public adopters (Swiss Re Assurance, CycloMedia, BUPA, Astonomer.io, cloudtrade)
- Presentation:
  - [KubeCon 2019 NA: KEDA: Event Driven and Serverless Containers in Kubernetes - Jeff Hollan, Microsoft](https://www.youtube.com/watch?v=ZK2SS_GXF-g)
  - [CloudBrew 2019: Event-driven computing with Kubernetes](https://www.cloudbrew.be/2019/#session-event-driven-computing-with-kubernetes)
  - Serverless Practitioners Summit 2020: Application Autoscaling Made Easy With Kubernetes Event-Driven Autoscaling (KEDA)

## Future Plans

KEDA continues to release every month, and with it a series of scaler improvements and overall quality improvements.  In addition to continuing to build out additional integrations, a few large features planned for the next year include:

- Enabling KEDA to scale StatefulSets
- Integration with SMI and service mesh for scaling
- Implement "duck-typing" for greater flexibility in our CRDs and scale capabilities
- Predictive scaling based on ML models and historic data

# Project Scope

## Clear project definition

KEDA is a single-purpose component for **Event Driven Autoscaling** of containers.  This provides serverless and reactive scale within any Kubernetes cluster.

## Alignment with CNCF mission

Kubernetes Event-driven Autoscaling (KEDA)'s mission is to make application autoscaling simple allowing Kubernetes users to focus on their workloads, not the scaling infrastructure. As part of that mission, we want to support as many customers as possible by being vendor neutral and are open to scale on any system.

The Kubernetes Event-driven Autoscaling (KEDA) project does not want to reinvent the wheel but build on standards instead and is complimentary to Kubernetes. Next to that, we have support for CNCF projects like Prometheus and NATS by providing scalers for them as well and package our product as a Helm chart (2.x & 3.x) which is available on Helm Hub. Lastly, we are vendor-neutral by supporting all major clouds and open-source technologies like Redis.

While the scaling features of Kubernetes Event-driven Autoscaling (KEDA) are important, we are a strong believer of making the product itself operable as well. By using Operator SDK we also want to allow operators to efficiently manage the infrastructure necessary to run Kubernetes Event-driven Autoscaling (KEDA) and are planning to provide a better operational experience as a whole by providing a CLI, dashboard, etc.

Security is one of our main focuses and we will keep on investing in that - This is why pod identity has been one of our main focuses for 1.0 and will continue to support more identity providers over time.

## Value-add to the CNCF ecosystem

The Kubernetes Event-driven Autoscaling (KEDA) project does not want to reinvent the wheel but build on standards instead and is complimentary to Kubernetes.

From the beginning intent was open and community driven (open community standups, MIT License, non-Microsoft branded). 

CNCF provides a vendor neutral home for key serverless capability.


## Alignment with other CNCF projects

KEDA augments and enhances many CNCF projects by adding event driven scale, including:

- Kubernetes itself (helping drive features back into things like the HPA / Cluster autoscaler)
- Virtual Kubelet
- NATS
- Promethues
- Strimzi
- Helm

## Anticipated use cases

- Serverless container and FaaS scaling
- Data processing pipelines
- Application scaling
- Batch processing

## Alignment with SIG Reference Model

SIG-Runtime

## High level architecture

KEDA performs two key roles within Kubernetes. First, it acts as an agent to activate and deactivate a deployment to scale to and from zero on no events. This is one of the primary roles of the keda-operator container that runs when you install KEDA.

Second, KEDA acts as a Kubernetes metrics server to expose rich event data like queue length or stream lag to the horizontal pod autoscaler to drive scale out. It is up to the deployment to then consume the events directly from the source. This preserves rich event integration and enables gestures like completing or abandoning queue messages to work out of the box. The metric serving is the primary role of the keda-operator-metrics-apiserver container that runs when you install KEDA.

![KEDA Architecture](https://i.imgur.com/lBVkWsH.png)

# Formal Requirements

Sponsors: TBD
