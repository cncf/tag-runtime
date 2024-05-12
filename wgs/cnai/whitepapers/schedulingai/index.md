---
title:  "Scheduling AI workloads on K8s TBD"
pdf: TBD
description: |
  TBD
type: whitepapers
url: /whitepapers/schedulingai
toc_hide: false
list_pages: true
weight: 3
---

[TOC]

## Executive Summary


## What's different about AI workloads

Kubernetes is great for microservices that scale out, and the default kube-scheduler works fine for them. But AI workloads need some extra features from a batch scheduler to manage them well.
- They often run tons of short tasks in parallel, using up all the resources they can get. The more resources they get, the faster they finish. The total resource usage is similar, but the job speed depends on how much resources they can grab.
- They create a lot of variation in the demand for resources, because there are many AI/ML jobs running every day or hour.
- They need distributed resources
- And GPUs are hard to come by and pricey.

## We need to update the job controller so that it handles the AI/ML workloads

Here's what we want to change: 
- We want to give users different priority levels, so they can use the right amount of GPUs, and also let lower priority users take advantage of any free GPUs.
- We want to improve how it pauses and resumes jobs based on the priority and policies, so we can handle changing demands and cluster load. For example, we want to kick out a lower priority user if a higher priority one needs a GPU.
- We want to use multiple queues to manage long running jobs better. This way, we can set up policies that make sense for the users, like how many GPUs they can use, how long they can wait, and what class of service they get. This is especially important for GPUs, since they are scarce and we don't want to waste them.
- We want to ensure fairness, so no job gets stuck because of heavy users, and everyone gets a fair share of the cluster.
- We want to use gang scheduling for jobs that need to run in parallel on multiple nodes. This means that the pods have to start and end together, even if they are on different nodes. This also helps with recovery, since we can restart the whole job if some pods fail, instead of the whole workload.
- We want to add elasticity, so we can start a job with whatever GPUs are available, even if it needs more, and then scale it up or down as GPUs become available or taken.

One thing you can do:
- [Mutable Scheduling Directives {Kubernetes v1.27 [stable]}](https://kubernetes.io/docs/concepts/workloads/controllers/job/#mutable-scheduling-directives) - This lets you tweak a Job's scheduling rules with the [suspend](https://kubernetes.io/docs/concepts/workloads/controllers/job/#suspending-a-job) field, so you can have more control over where the pods go (for custom queue controllers)

## How to improve the default kube-scheduler

We need a better scheduler for our Kubernetes clusters. It should place PODs or groups of PODs on the right nodes, taking into account things like co-location, affinity, co-scheduling, etc. Here are some of the improvements we want:- 
- Bin packing and consolidation - We want to use GPUs more efficiently by putting pods on busy nodes instead of random ones.
- Topology awareness within a node. The scheduler should know the layout of the nodes, the resources inside them, and which ones are free at any time.

Some things you can do:
- Node pools - We can group nodes with different GPUs using node pools and manage them better that way.
- Node proximity - Maybe the cloud providers can take care of the node topology and put them in close proximity, like using proximity settings for the worker node topology.
- [Dynamic Resource Allocation {Kubernetes v1.27 [alpha]}](https://kubernetes.io/docs/concepts/scheduling-eviction/dynamic-resource-allocation/) - This feature lets us create mini-GPUs (MIGs) on the fly as we need them.

## Workloads personas

We have researchers and data scientists

## Different GPU workload types

We have different GPU workload types 
- Training workloads that run for a long time
- Inference workloads that handle user requests from multiple users
- Short duration single user workloads
