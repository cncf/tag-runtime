# Container Orchestrated Device Working Group Charter

COD, the Container Orchestrated Device Working Group, is a small group formed by passionate Container Runtime Maintainers and Device Vendors looking to solve many of the challenges Devices face in the cloud native space.
 
* In today’s cloud native space, the support for Third Party Devices such as FPGAs, GPUs and others is fragmented, uneven and inconsistent. For example:
* Kubernetes supports Device Plugins
* Nomad has its own concept of Device Plugins
* Docker has an in tree plugin mechanism
* Podman has a concept of hooks 
* LXC has its own concept of hooks
* ...
 
From a user's perspective, the support for devices is widely different from one runtime to another and often requires painful setup and configuration.
Users also face the fact that container orchestrators also implement plugins for devices, leading to a different deployment story and level of support than they have at the runtime level.
 
From a vendor’s perspective, each plugin mechanism has a different set of capabilities leading plugin authors to either have to re-implement their plugins (leading to maintainability hell), resort to hacks or simply not support runtimes they should easily be able to support (e.g: Podman support but no Docker support).

## Goal

The Container Orchestrated Workging Group aims to improve the support of Devices in the cloud native space. 

# Projects
 
## Project #1: Container Device Interface
 
The Container Device Interface (CDI) is the first project the group focuses on and is a specification, for container runtimes, to support third party devices through a commonly understood plugin system (based on the CNI model).
 
### Concrete Deliverables
The main deliverable for CDI is a specification that runtimes can implement to enable containers to become device aware.
A secondary deliverable is a golang interface, with a package that can be re-used to merge the specification as well as a validation schema.
 
### Target User Stories

(Consistent UX) As a user, my experience across runtimes should be fairly consistent
(Standard Interface) As a plugin author, I should be focusing on my plugin’s features not adding support for similar runtimes
(Simple Model) As a cluster or system administrator, my experience installing plugins should be simple (e.g: run a container, install a package, deploy a pod, …)
(Ease of Deployment) Solve the difficulties faced by users in the cloud-native space
(Consistency) As a user, my experience interacting with runtimes should be fairly consistent
 
### Slides

[Container Device Interface Slides](https://docs.google.com/presentation/d/1UXgKYx5AA9ThYYLDswHsXFDL7TrNzVcac8zjlMIfEDs/)


# General Information

## Stakeholder TAG

TAG Runtime

## Meetings

* Every other Tuesday at 7am PST. [Convert to your timezone](http://www.thetimezoneconverter.com/?t=07:00&tz=PT%20%28Pacific%20Time%29).
* Link to [Google Doc Notes](https://docs.google.com/document/d/1gUgAMEThkRt4RJ7pA7ZbPPmIOX2Vb7fwH025MjfcTYU/edit?ts=5ef21262#)


## WG Chairs

* Alexander Kanevskiy ([@kad](https://gihub.com/kad)), Intel
* Evan Lezar ([@elezar](https://github.com/elezar)), NVIDIA

## WG Members

* Urvashi Mohnani ([@umohnani8](https://gihub.com/umohnani8)) 
* Ed Bartosh
* Ukri Niemimuukko
* Marek Counts 
* Mike Brown, IBM
* Mrunal Patel

## WG Emeretus chair

* Renaud Gaubert ([@RenaudWasTaken](https://github.com/RenaudWasTaken)), NVIDIA

## Slack

#tag-runtime

## Mailing List

https://lists.cncf.io/g/cncf-tag-runtime

# Related Information
 
* [Container Device Interface Slides](https://docs.google.com/presentation/d/1UXgKYx5AA9ThYYLDswHsXFDL7TrNzVcac8zjlMIfEDs/)
* Networking Plumbing Working Group - NPWG
  * https://docs.google.com/document/d/1oE93V3SgOGWJ4O1zeD1UmpeToa0ZiiO6LqRAmZBPFWM
  * https://docs.google.com/document/d/1rBm-L1ymXIjoKNA6w2lixwBAjt9-tnbs-ee7AcLRbVE
  * https://docs.openstack.org/kuryr-kubernetes/latest/specs/rocky/npwg_spec_support.html
