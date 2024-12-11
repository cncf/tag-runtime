---
title: Special Purpose Operating System Working Group Charter
--- 
## Background

Special Purpose Operating Systems are designed to run well defined workloads with minimal boilerplate of dependencies suited for niche use cases. 

In the cloud native world, these workloads include containers, however, they can be extended to other special purpose workloads such as WASM, etc. 

## Mission Statement

The special purpose operating system working group (wg-sp-os) focuses on the operations, best practices and guidance on running cloud native workloads on operating systems, including, but not limited to containers, across orchestrators such as Kubernetes and other cloud-native projects. The immediate focus of the working group will be to work on container OSs, however, other areas such as WASM would still be part of the charter of the working group. For future cloud native related efforts, the charter of the working group would be extended upon consensus in the community. The working group aims to:
- Foster an ecosystem for collaboration between existing projects
- Educate users with unbiased and common understanding of special purpose OSs
- Identify gaps in the landscape and attract new projects to the ecosystem

## Scope

The working group is focused on the following areas:
Guidance on Cloud Native practices for Container OSs which include:
- Lifecycle and configuration management
- Resource utilization
- Upgrade scenarios
- Long Term Support constraints
- Compatibility with container runtimes
- Flexibility and interoperability with container orchestration solutions which includes Compatibility with kubelet API versus host dbus/systemd in the case of Kubernetes workloads
- Best practices for security considerations for cloud native container os workloads
- Best practices for integration with softwares designed for management and monitoring of the hosts, such as antivirus agents. 

## Deliverables 

- Publications, presentations, and whitepapers on areas related to running cloud native workloads on special purpose OSs
   - Potential whitepaper ideas:
      - Guidance on LTS: How does LTS in Kubernetes impact special purpose/container OSs?
      - What is a container operating system for cloud native workloads?
- Integration with the Kubernetes project
   - Exploring the area of providing an interface for OS in Kubelet, similar to CNI or CSI. A single interface to work with Kubelet to work across distributions.
- Guidance on usage and technical support for running container workloads on OSs
- Exploration and looking beyond the horizon of container workloads and incorporating other workloads such as WASM on special purpose OSs with close collaboration with WASM Working Group.
- Collaboration within the community on related areas like edge computing, etc
- Collaboration for any fixes or contributions to upstream projects like the Linux kernel
- Integration with other projects in the community like Cluster API
   - Exploring the area for a standard abstraction for special purpose OSs to interact with Cluster API, with respect to bootstrap providers, etc.
- Metrics - provides guidelines for project planning in terms of resource usage.
- Ecosystem updates - provides updates on the landscape of cloud-native projects on the special purpose OSs at conferences, in publications, and to the TAG Runtime.

## Open Source Projects

Following is a list of popular open-source projects that are in the container OS space:
- [Bottlerocket](https://bottlerocket.dev)
- [Flatcar](https://www.flatcar.org)
- [Talos](https://www.talos.dev)
- [Kairos](https://kairos.io)
- [openSUSE MicroOS](https://microos.opensuse.org/)
- [Google’s Container Optimized OS (COS)](https://cloud.google.com/container-optimized-os/docs/resources/sources)

## Operations
This WORKING GROUP follows the [standard operating guidelines](https://github.com/cncf/toc/blob/main/tags/cncf-tags.md#operating-model) provided by the TOC unless otherwise stated here.

## TAG Liaison
- [Rajas Kakodkar](https://github.com/rajaskakodkar)

## TOC Liaison
- [Nikhita Raghunath](https://github.com/nikhita)

## Chairs
- [Danielle Tal](https://github.com/miao0miao)
- [Sean McGinnis](https://github.com/stmcginnis)
- [Mauro Morales](https://github.com/mauromorales)


## Technical Leaders
- [Thilo Fromm](https://github.com/t-lo)

## Communication

- **Community Meeting:** Monthly, 1st Thursday of the Month at 2:00 PM UTC [(convert to your timezone)](https://dateful.com/convert/coordinated-universal-time-utc?t=2pm)
- **Zoom Link for the meeting:**  [Click here](https://zoom.us/my/cncftagruntime?pwd=N2xyRkZaN2JWZkNmS3EzbE1HVnhEQT09) , Passcode: 77777
- **Meeting Notes and Agenda:** [Click here](https://docs.google.com/document/d/1MeFwrnOeleTazqmZe16p0fEFLiLPgtCIAAOFIatWNsg/)
- **CNCF Slack:** [#wg-sp-os](https://slack.cncf.io/#wg-sp-os)
- **Mailing list:** https://lists.cncf.io/g/cncf-tag-runtime
- **Meeting recordings:** [youtube channel](https://www.youtube.com/watch?v=zjvfHmb37tQ&list=PL6wYrb-bYwC_1pcrKc4NdilT6YeyqFtB7&ab_channel=CNCFTAGRuntime)

## Document Reviewed and Contributed by
- [Ettore Di Giacinto](https://github.com/mudler)
- [Justin Haynes](https://github.com/jhaynes)
- [Nikhita Raghunath](https://github.com/nikhita)
- [Priyanka Saggu](https://github.com/Priyankasaggu11929)
- [Rajas Kakodkar](https://github.com/rajaskakodkar)
- [Sean McGinnis](https://github.com/stmcginnis)
