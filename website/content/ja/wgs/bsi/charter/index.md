---
title: クラウドネイティブバッチシステムワーキンググループチャーター
---

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
follow this specification to work with projects in CNCF, e.g. Kubernetes, Volcano, Armada,
or even out of CNCF, e.g. YuniKorn and MCAD and others.

## Goal:

The Cloud Native Batch System Initiative Working Group aims to define
batch system specifications in the cloud native ecosystem for different batch projects,
and related CRDs, gRPC, client libraries for projects. Those outputs will help related projects
to figure out their scopes, and identify the different scenarios for different projects, e.g. traditional HPC vs. HPC on Cloud.

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

- [Volcano](https://volcano.sh/)
- [Kubernetes](https://kubernetes.io/)
- [YuniKorn](https://yunikorn.apache.org/)
- [Kubernetes WG Batch](https://github.com/kubernetes/community/blob/master/wg-batch/charter.md)
- Etc.

## Operations

This Batch System Initiative Working Group follows the [standard operating guidelines](https://github.com/cncf/toc/blob/main/tags/cncf-tags.md#operating-model) provided
by the TOC unless otherwise stated here.

- TOC Liaisons: Ricardo Rocha (ricardo.rocha@cern.ch)
- SIG Chairs: 
  - Marlowe Warnicke (catblade+batch@gmail.com)
  - Abhishek Malvankar (abhishekmalvankar9@gmail.com)
  - Alex Scammon (alex@gr-oss.io)

## Communities

- Meeting Schedule: Twice a month on the 1st and 3rd Thu at 8am PDT/PST
- [Meeting Invite](https://calendar.google.com/calendar/event?action=TEMPLATE&tmeid=aTBka2F2aWt2ZTM0aTZuaG40MXRhdHM2dHNfMjAyMzA5MTFUMTUwMDAwWiBjXzY1MjRkNjA2OWI0YjczZDY1NGE2ZGFkYmFjNmQzMWRhMmU3NzZkOWNhMGRkZGY4OGFiMTJlMjZiODc1NzBhODJAZw&tmsrc=c_6524d6069b4b73d654a6dadbac6d31da2e776d9ca0dddf88ab12e26b87570a82%40group.calendar.google.com&scp=ALL)
- Mailing list: cncf-wg-bsi@googlegroups.com 
- Slack channel:  https://cloud-native.slack.com/archives/C02Q5DFF3MM
