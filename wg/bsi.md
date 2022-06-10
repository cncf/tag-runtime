# Cloud Native Batch System Initiative Working Group Charter
 
## Introduction

Cloud Native Batch System Initiative Working Group is a group formed by 
passionate batch system maintainers looking to support batch workload in cloud native environments.
 
## Background

Currently, more and more users would like to migrate batch workloads to cloud native environments,
and multiple existing solutions from different community projects currently address this requirement,
e.g. Volcano, YuniKorn, Armada, MCAD, which makes it easy for users to migrate.
But from a user perspective, the current support for batch workloads is widely different from 
one batch system to another and requires a comprehensive migration between them. 
It’s necessary to build a specification for batch workloads in the cloud native ecosystem, 
and help related projects figure out their scopes and interaction. The users and communities can 
follow this specification to work with projects in CNCF, e.g. Kubernetes, Volcano, Armada, MCAD, 
or even out of CNCF, e.g. YuniKorn, and so on.
  
## Goal:

The Cloud Native Batch System Initiative Working Group aims to define
batch system specifications in the cloud native ecosystem for different batch projects,
and related CRDs, gRPC, client libraries for projects. Those outputs will help related projects
to figure out their scopes, and identify the different scenarios for different projects, e.g. tranditional HPC vs.
HPC on Cloud.
   
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

- Kubernetes
- Volcano
- YuniKorn
- Armada
- Slurm
- Htcondors
- others

## Operations

This Batch System Initiative Working Group follows the [standard operating guidelines](https://github.com/cncf/toc/blob/main/tags/cncf-tags.md#operating-model) provided
by the TOC unless otherwise stated here.

- TOC Liaisons: Ricardo Rocha (ricardo.rocha@cern.ch)
- SIG Chairs: Klaus Ma (klaus1982.cn@gmail.com), Weiwei Yang (abvclouds@gmail.com), Alex Scammon (alex@gr-oss.io)

## Communities

- Meeting Schedule: Twice a month on the 1st and 3rd Thu at 
- Mailing list: cncf-tag-runtime@lists.cncf.io 
- Slack channel:  https://cloud-native.slack.com/archives/C02Q5DFF3MM 

