---
title: Cloud Native Batch System Initiative Working Group Charter
weight: 1
---
 
## Introduction

The Cloud Native Batch System Working Group is a collective of dedicated batch system maintainers focused on advancing support for batch workloads in cloud-native environments.
 
## Background

The demand for migrating batch workloads to cloud-native environments continues to grow. Several community-driven solutions, including Volcano, YuniKorn, Armada, and MCAD, already address this need, simplifying migration for users. However, the capabilities and approaches among these systems vary significantly, creating challenges for users seeking a unified and consistent experience.

While existing batch scheduling systems effectively address scheduling concerns, batch workload management requires a holistic approach that considers the entire system, including storage, networking, and cost optimization. These interconnected aspects are crucial to delivering efficient and scalable batch processing in cloud-native environments.

To address these challenges, it is essential to foster alignment among the various stakeholders in the batch scheduling ecosystem. This alignment will focus on establishing a shared direction for how batch scheduling should evolve in a cloud-native context. While this process may result in specifications, protocols, and standards, the primary goal is to ensure ongoing collaboration and coordination across projects within CNCF and external ecosystems. By bringing these parties together, we aim to create a foundation for consistent, efficient, and user-focused batch workload solutions.
  
## Goal:

The Cloud Native Batch System Working Group aims to:

 - Foster collaboration and alignment among batch system projects, ensuring a consistent and user-friendly experience for batch workload management.
 - Provide guidance on best practices for batch scheduling in cloud-native environments.
 - Establish a common understanding of batch system requirements, enabling users to navigate the batch scheduling landscape with confidence.
 - Develop standardized specifications for batch systems within the cloud-native ecosystem.
 - Define essential components such as Custom Resource Definitions (CRDs), gRPC APIs, and client libraries to support these standards.
 - Clarify the scopes and use cases of various batch projects, helping distinguish between scenarios like traditional HPC and cloud-native HPC.

These deliverables will enhance collaboration among projects, improve interoperability, and empower users to efficiently leverage batch systems in cloud-native environments.
   
## In Scope:

Batch system specifications, including:

- Job/ArrayJob/CronJob
- Job Flow/Job Dependency/Job Orchestration
- Queue
- SchedulingPolicy (e.g. PodGroup)
- Command Line & Script
- Multi-Cluster Scheduling
- Best Practices

## Out Of Scope:

- Non-batch related workloads
- The implementation of the batch system

## Related Communities

This Working Group will be reaching out and requesting/receiving feedback from other communities and working groups on a regular basis (not limited to):

- [Current Batch System Projects Landscape](https://tag-runtime.cncf.io/wgs/bsi/landscape/)
  - This landscape provides an overview of the batch system projects that are currently active in the cloud-native ecosystem.
- [Kubernetes WG Batch](https://github.com/kubernetes/community/blob/master/wg-batch/charter.md)
  - Because it is often a point of confusion, there are two "Batch Working Groups": 
    - the one for the CNCF -- this one -- which is focused on batch scheduling in the cloud-native ecosystem
    - the one for Kubernetes -- our sister group -- which focuses more specifically on lower-level changes to Kubernetes that are required for Kubernetes to support batch scheduling generally.
  - The Kubernetes Working Group for Batch Scheduling is a key partner in the cloud-native batch scheduling ecosystem. By collaborating with this group, we aim to align our efforts with the broader Kubernetes community and ensure that our work complements existing batch scheduling initiatives.

## Operations

This Batch System Initiative Working Group follows the [standard operating guidelines](https://github.com/cncf/toc/blob/main/tags/cncf-tags.md#operating-model) provided
by the TOC unless otherwise stated here.

- TOC Liaisons: Ricardo Rocha (ricardo.rocha@cern.ch)
- SIG Chairs: 
  - Marlowe Warnicke (catblade+batch@gmail.com)
  - Abhishek Malvankar (abhishekmalvankar9@gmail.com)
  - Alex Scammon (alex@gr-oss.io)

## Communities

- Meeting Schedule: Every other Tuesday at 8am PDT/PST
- [Meeting Invite](https://calendar.google.com/calendar/event?action=TEMPLATE&tmeid=bWlmY2h1NmE2MmMxcnU1cjgzc3RvcjV0bW9fMjAyNTAyMTFUMTYwMDAwWiBjXzY1MjRkNjA2OWI0YjczZDY1NGE2ZGFkYmFjNmQzMWRhMmU3NzZkOWNhMGRkZGY4OGFiMTJlMjZiODc1NzBhODJAZw&tmsrc=c_6524d6069b4b73d654a6dadbac6d31da2e776d9ca0dddf88ab12e26b87570a82%40group.calendar.google.com&scp=ALL)
- Mailing list: cncf-wg-bsi@googlegroups.com 
- Slack channel:  https://cloud-native.slack.com/archives/C02Q5DFF3MM 