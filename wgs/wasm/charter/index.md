---
title: WebAssembly (Wasm) Working Group Charter
---
## Background

WebAssembly, commonly known as Wasm, refers to a compact binary instruction format utilized by a stack-based virtual machine. Its primary purpose is to serve as a versatile compilation target for programming languages, enabling seamless deployment of applications for both client-side and server-side environments.

In the context of cloud native, and with the presence of a Wasm runtime, the portability and versatility of Wasm allow users to run workloads in a diverse set of environments in both a centralized location and at the edge, including but not limited to VMs running a single docker daemon, Kubernetes cluster, and any other compatible workload orchestrator.

## Mission Statement

The Wasm working group focuses on topics of running Wasm workloads across the edge, Kubernetes, and other cloud-native projects. The primary mission is to enable Wasm to be a first-class alternative to running such workloads. The secondary mission is to ensure Wasm is integrated and evolved across all cloud-native projects. We do so by promoting the adoption and usage of WebAssembly by providing resources, best practices, and tools that enable end users to utilize its unique benefits.

## Scope

The working group is interested in all topics related to building Wasm artifacts, packaging and distribution, and developing solutions that embrace Wasm, including:

- Developing and adjusting **infrastructure for Wasm deployments**. The cloud-native modifications to meet Wasm conditions. 
- Development and configuration of **wasm-specific workloads**. How do we start working with Wasm? How do we write,  deploy, test and debug our workloads to Wasm environments? How do we empower Wasm to those specific ML/AI workloads with a wide variety of AI HW accelerators? 
- Cloud-native **DevOps practices for Wasm** environments. How do we operate our workloads in Wasm deployment scenarios? Typical DevOps and Observability topics need to be adjusted to Wasm environments.
- **Interoperability** with other deployment types. Wasm workloads should be able to run in a pod alongside containers seamlessly.
- **Security** - Understanding, documenting, and educating folks on the security considerations of their WASM and WASI workloads and how to integrate WASM runtimes into their projects safely.
- **Wasm artifacts** - guide and document container registry storage structures to provide a basis for compatibility for container runtimes.

## Deliverables

The working group will build collaboration, knowledge, and projects in the Wasm space, including:
 			
- **Publications, presentations, and whitepapers** on interesting topics - the group will stay ahead of the current technology trends and provide material on the latest innovative topics in the space.
- **Example architectures and demos** - provides well-documented use cases using existing projects and demos that can be used as starting points for future projects.
- **Standards, tests, and certifications** - the working group will investigate if it is possible to certify solutions in well-defined domains against known criteria.
- **WebAssembly ecosystem proposals** - provide updates on the different open proposals and how they benefit the ecosystem. Collaborate and align with the community on the current and new proposals. 
- **Metrics** - provides guidelines for project planning in terms of resource usage.
- **Ecosystem updates** - provides updates on the landscape of cloud-native projects on the Wasm at conferences, in publications, and to the Runtime TAG.
- **Vertical Use cases** - provide documentation or code implementation of cloud-native wasm use cases in certain vertical scenarios (network, database, AI, embedding a Wasm runtime, etc.)

## Projects

### Current CNCF Wasm-centric projects

The following is a list of well-known CNCF projects built by or integrates with Wasm:

- **Runtime related**

    - [WasmEdge](https://wasmedge.org/)
    - [WasmCloud](https://github.com/wasmcloud/)
    - [Runwasi](https://github.com/containerd/runwasi)
    - [Krustlet](https://github.com/krustlet/krustlet)
    - [Kuasar](https://github.com/kuasar-io/kuasar) - Kubernetes Container Runtime Engine supports Wasm
    - [Dapr](https://dapr.io) - both embedded Wasm in sidecar runtime as well as Wasm SDK to access the sidecar service from Wasm apps. 
    - [crun](https://github.com/containers/crun)
    - [youki](https://github.com/containers/youki)
    - [Docker](https://docs.docker.com/desktop/wasm/)

- **Other CNCF scopes**

    - [Open Policy Agent](https://github.com/open-policy-agent/opa) - can compile policies to wasm files
    - [Envoy](https://github.com/envoyproxy/envoy)/[Istio](https://github.com/istio/istio) (Wasm filter)
    - [KubeWarden](https://github.com/kubewarden) - Kubernetes policy engine; policies compiled to WebAssembly
    - [Knative](https://knative.dev/docs/)
    - [KubeEdge](https://kubeedge.io/en/)
    - [OpenFunction](https://openfunction.dev)
    - [SuperEdge](https://superedge.io)

Note that even though this group is under TAG-Runtime, there may be other areas to interface as indicated above.

### Open Source (non-CNCF) Wasm Projects

A list of notable, popular, and/or influential open-source Wasm projects that are in the cloud native space but not necessarily officially part of the CNCF (Runtime and non-runtime related):

- [Wasmer](https://wasmer.io/)
- [Suborbital](https://suborbital.dev/)
- [Spin](https://github.com/fermyon/spin)
- [Wazero](https://wazero.io/)
- [extism](https://extism.org)
- [wasmtime](https://wasmtime.dev)
- [WasmLabs](https://wasmlabs.dev) at VMWare
- [Javy](https://github.com/bytecodealliance/javy)
- [SpiderLightning (Slight)](https://github.com/deislabs/spiderlightning)

## Operations

This WORKING GROUP follows the [standard operating guidelines](https://github.com/cncf/toc/blob/main/tags/cncf-tags.md#operating-model) provided by the TOC unless otherwise stated here.

### TAG Liaison
- [Ricardo Aravena](https://github.com/raravena80)
- [Heba Elayoty](https://github.com/helayoty)

### TOC Liaison
- [Nikhita Raghunath](https://github.com/nikhita)

### WG Chairs
- [David Justice](https://github.com/devigned)
- [Danielle Lancashire](https://github.com/endocrimes)
- [Taylor Thomas](https://github.com/thomastaylor312)


### WG Technical Leaders
- [Angel M Miguel](https://github.com/Angelmmiguel)
- [Kevin Hoffman](https://github.com/autodidaddict)
- [Sven Pfennig](https://github.com/0xE282B0)

## Communication

- **Community Meeting** (Pacific Time): Fortnightly, Tuesdays at 5:00 pm CEST - [Calendar](https://tockify.com/cncf.public.events/monthly?search=Wasm%20WG)
- **Meeting Notes and Agenda**: [Click here](https://docs.google.com/document/d/1d6PvdCuKbSdcuXG2M9fBSDQPTPfHYA0PPDTM2plbH3I)
- **CNCF Slack**: [#wg-wasm](https://cloud-native.slack.com/archives/C056EDRH4PJ)
- **Mailing list**: https://lists.cncf.io/g/cncf-tag-runtime 

### Charter Reviewed and Contributed by
- [Angel M Miguel](https://github.com/Angelmmiguel)
- [Danielle Lancashire](https://github.com/endocrimes)
- [David Justice](https://github.com/devigned)
- [Heba Elayoty](https://github.com/helayoty)
- [Ismo Puustinen](https://github.com/ipuustin)
- [Jiaxiao (Joe) Zhou](https://github.com/Mossaka)
- [Michael Yuan](https://github.com/juntao)
- [Mikkel Mork](https://github.com/mikkelhegn)
- [Ralph Squillace](https://github.com/squillace)
- [Ravikanth Chaganti](https://github.com/rchaganti)
- [Ricardo Aravena](https://github.com/raravena80)
- [Toru Komatsu](https://github.com/utam0k)
- [Tiejun Chen](https://github.com/TiejunChina)
- [Shivay Lamba](https://github.com/shivaylamba)
- [Sven Pfennig](https://github.com/0xE282B0)
