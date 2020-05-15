# CNCF SIG-Runtime Metal<sup>3</sup> Sandbox Review and Recommendation


## Acceptance to CNCF Sandbox

Authors: Ricardo Aravena

Reviewed by: Klaus Ma, Diane Feddema, Alena Prokharchyk, Quinton Hoole


# Background

[Link to TOC PR](https://github.com/cncf/toc/pull/408)

[Link to Presentation](https://youtu.be/SuRUtlSQbm4)

[Link to GitHub project](https://github.com/metal3-io)


## Project Goal

The Metal³ project provides bare metal host management for Kubernetes. Also, a subset of Metal³ can be used to perform bare metal host provisioning for any purpose.


## Current Status

The project is in active status with maintainers from Ericsson, Mirantis and Red Hat. It also has committers from the following organizations: AT&T, Dell EMC, Ericsson, Fujitsu, Mirantis and Red Hat. The two main components of the project have these commit author numbers:



*   baremetal-operator has 38 commit authors
*   cluster-api-provider-metal3 has 20 commit authors


## Future Plans

At a high level:



*   Focus more on production use cases and the required quality.
*   Maturing cluster-api support and staying current with cluster-api API changes.
*   Expanding bare metal host management capabilities in the BareMetalHost API (such as RAID configuration)
*   Explore support of other provisioning approaches (currently relies on PXE, the project wants to expose virtual media based deployments)


# Project Scope


## Clear project definition

**_Does the project have a clear and well defined scope?_**

Metal<sup>3</sup> is defined as a project that allows users to deploy bare-metal Kubernetes nodes as well as regular bare-metal nodes. The scope is clear as to what the use case is. It also has two main components:



1. Kubernetes Operator, that manages the bare metal nodes.
2. Cluster-API Component to provision nodes.


## Value-add to the CNCF ecosystem

**_Does the project have a clear value add to the current project ecosystem? How does it relate to other projects with overlapping capabilities? _**

Metal<sup>3</sup> fills a gap in the CNCF project ecosystem. Currently, there are no CNCF projects that allow users to provision bare-metal machines either with Kubernetes or as standalone. Also, this would be a good complement to the Kubernetes ecosystem for those users that would like to provision bare-metal nodes. 

A unique use case would be provisioning bare-metal nodes to allow Kubernetes to run VM based runtimes such as [Kata Containers](https://katacontainers.io/) or [Firecracker](https://firecracker-microvm.github.io/). Other potential future technologies that could take advantage of this project are:



*   [cloud hypervisor](https://github.com/cloud-hypervisor/cloud-hypervisor): an open source Virtual Machine Monitor (VMM) that runs on top of KVM and focuses on exclusively running modern, cloud workloads, on top of a limited set of hardware architectures and platforms.
*   [Bottlerocket](https://github.com/bottlerocket-os/bottlerocket): an open source Operating System for container hosting.


## Alignment with other CNCF projects

**_Does the project align and actively collaborate with other CNCF projects? _**

Metal<sup>3</sup> aligns with other SIG-Runtime projects.



*   CRI-O: The runtime shim can be used in the bare-metal nodes
*   Containerd: the runtime shim can be used in bare-metal nodes.
*   Kubernetes can use this project to provision bare-metal Kubernetes nodes.


## Alignment with SIG-Runtime

Metal<sup>3</sup> falls within the SIG-Runtime scope because one of SIG-Runtime’s focus is mechanisms or projects that allow the use of cloud native workloads and bare-metal machines are used to run those cloud native workloads.


## High level architecture

This is the original high level architecture diagram:



![high_level_arch](https://github.com/metal3-io/metal3-docs/blob/master/images/high-level-arch.png "High Level Arch")


Bare-metal operator components diagram:



![OperatorComponents](https://user-images.githubusercontent.com/7659560/82079853-68764c00-9698-11ea-9654-b0e85bc247de.png)



Cluster API Integration + Bootstrap cluster:


![ClusterAPIIntegration](https://user-images.githubusercontent.com/7659560/82079935-86dc4780-9698-11ea-941e-8b07bb297f34.png)


Cluster API Provider:


![ClusterAPIProvider](https://user-images.githubusercontent.com/7659560/82080162-e63a5780-9698-11ea-9d80-6c69133f454f.png)


For a more detailed description of all the components you can refer to the [project’s documentation](https://metal3.io/documentation.html).


# Formal Requirements

**_Document that the project fulfills the requirements as documented in the [CNCF graduation criteria](https://github.com/cncf/toc/blob/master/process/graduation_criteria.adoc)_**


## Sandbox Stage

As Metal<sup>3</sup> is submitted at the sandbox stage it needs to meet the following criteria. 



*   Metal<sup>3 </sup>is requesting 3 TOC sponsors
*   Metal<sup>3 </sup>will adopt the CNCF [Code of Conduct](https://github.com/cncf/foundation/blob/master/code-of-conduct.md)
*   Metal<sup>3 </sup>will adhere to CNCF [IP Policy](https://github.com/cncf/foundation/blob/master/charter.md#11-ip-policy) (including trademark transferred)


# CNCF IP Policy



*   [Metal3 bare-metal operator](https://github.com/metal3-io/baremetal-operator) (Apache 2.0)
    *   The operator uses [openstack-ironic](https://wiki.openstack.org/wiki/Ironic). This component is open source and [its license](https://opendev.org/openstack/ironic/src/branch/master/LICENSE) is Apache 2.0. A per the CNCF IP policy: “CNCF project dependencies that are licensed under Apache-2.0 do not require further license review or approval, since they are under the same license as the CNCF project itself.”
*   [Metal3 cluster API provider](https://github.com/metal3-io/cluster-api-provider-metal3) (Apache 2.0)

Dependencies for baremetal-operator:



*   github.com/PuerkitoBio/urlesc BSD-3-Clause
*   golang.org/x/text BSD-3-Clause
*   github.com/evanphx/json-patch BSD-3-Clause
*   go.uber.org/atomic MIT
*   github.com/gophercloud/gophercloud Apache-2.0
*   golang.org/x/xerrors BSD-3-Clause
*   github.com/PuerkitoBio/purell BSD-3-Clause
*   gopkg.in/fsnotify.v1 BSD-3-Clause
*   cloud.google.com/go/compute/metadata Apache-2.0
*   github.com/emicklei/go-restful MIT
*   sigs.k8s.io/controller-runtime/pkg Apache-2.0
*   github.com/go-openapi/spec Apache-2.0
*   k8s.io/apimachinery Apache-2.0
*   github.com/matttproud/golang_protobuf_extensions/pbutil Apache-2.0
*   github.com/hashicorp/golang-lru MPL-2.0
*   gopkg.in/yaml.v2 Apache-2.0
*   golang.org/x/net BSD-3-Clause
*   github.com/go-logr/logr Apache-2.0
*   gomodules.xyz/jsonpatch/v2 Apache-2.0
*   github.com/go-openapi/swag Apache-2.0
*   k8s.io/api Apache-2.0
*   github.com/go-openapi/jsonreference Apache-2.0
*   k8s.io/client-go Apache-2.0
*   github.com/imdario/mergo BSD-3-Clause
*   github.com/mailru/easyjson MIT
*   github.com/go-logr/zapr Apache-2.0
*   github.com/golang/groupcache/lru Apache-2.0
*   github.com/beorn7/perks/quantile MIT
*   github.com/golang/protobuf BSD-3-Clause
*   github.com/prometheus/common/internal/bitbucket.org/ww/goautoneg BSD-3-Clause
*   golang.org/x/sys/unix BSD-3-Clause
*   github.com/spf13/pflag BSD-3-Clause
*   github.com/gogo/protobuf BSD-3-Clause
*   github.com/google/gofuzz Apache-2.0
*   github.com/pkg/errors BSD-2-Clause
*   sigs.k8s.io/yaml MIT
*   github.com/modern-go/reflect2 Apache-2.0
*   golang.org/x/time/rate BSD-3-Clause
*   gopkg.in/inf.v0 BSD-3-Clause
*   github.com/json-iterator/go MIT
*   github.com/davecgh/go-spew/spew ISC
*   golang.org/x/oauth2 BSD-3-Clause
*   github.com/metal3-io/baremetal-operator Apache-2.0
*   go.uber.org/multierr MIT
*   github.com/prometheus/client_golang/prometheus Apache-2.0
*   github.com/modern-go/concurrent Apache-2.0
*   github.com/cespare/xxhash/v2 MIT
*   github.com/prometheus/procfs Apache-2.0
*   golang.org/x/crypto/ssh/terminal BSD-3-Clause
*   github.com/google/uuid BSD-3-Clause
*   github.com/go-openapi/jsonpointer Apache-2.0
*   k8s.io/klog Apache-2.0
*   k8s.io/kube-openapi/pkg Apache-2.0
*   go.uber.org/zap MIT
*   github.com/prometheus/client_model/go Apache-2.0
*   github.com/googleapis/gnostic Apache-2.0
*   github.com/prometheus/common Apache-2.0
*   k8s.io/utils Apache-2.0
*   github.com/google/go-cmp/cmp BSD-3-Clause
*   github.com/operator-framework/operator-sdk Apache-2.0

Dependencies for cluster-api-provider-metal3



*   github.com/modern-go/concurrent Apache-2.0
*   github.com/google/uuid BSD-3-Clause
*   golang.org/x/text BSD-3-Clause
*   github.com/pkg/errors BSD-2-Clause
*   gomodules.xyz/jsonpatch/v2 Apache-2.0
*   github.com/PuerkitoBio/urlesc BSD-3-Clause
*   github.com/golang/mock/gomock Apache-2.0
*   github.com/docker/distribution Apache-2.0
*   k8s.io/klog Apache-2.0
*   github.com/evanphx/json-patch BSD-3-Clause
*   github.com/matttproud/golang_protobuf_extensions/pbutil Apache-2.0
*   github.com/opencontainers/go-digest Apache-2.0
*   github.com/go-openapi/spec Apache-2.0
*   github.com/metal3-io/cluster-api-provider-metal3 Apache-2.0
*   k8s.io/api Apache-2.0
*   github.com/blang/semver MIT
*   sigs.k8s.io/controller-runtime Apache-2.0
*   golang.org/x/oauth2 BSD-3-Clause
*   github.com/hashicorp/golang-lru MPL-2.0
*   github.com/golang/groupcache/lru Apache-2.0
*   github.com/prometheus/common Apache-2.0
*   github.com/mailru/easyjson MIT
*   github.com/gogo/protobuf BSD-3-Clause
*   github.com/davecgh/go-spew/spew ISC
*   github.com/modern-go/reflect2 Apache-2.0
*   gopkg.in/yaml.v2 Apache-2.0
*   github.com/spf13/pflag BSD-3-Clause
*   k8s.io/apimachinery Apache-2.0
*   golang.org/x/time/rate BSD-3-Clause
*   github.com/metal3-io/baremetal-operator/pkg/apis Apache-2.0
*   github.com/PuerkitoBio/purell BSD-3-Clause
*   k8s.io/cluster-bootstrap/token Apache-2.0
*   golang.org/x/crypto/ssh/terminal BSD-3-Clause
*   github.com/json-iterator/go MIT
*   github.com/imdario/mergo BSD-3-Clause
*   github.com/go-openapi/swag Apache-2.0
*   github.com/go-logr/logr Apache-2.0
*   k8s.io/apiextensions-apiserver/pkg/apis/apiextensions Apache-2.0
*   github.com/go-openapi/jsonpointer Apache-2.0
*   gopkg.in/fsnotify.v1 BSD-3-Clause
*   gopkg.in/inf.v0 BSD-3-Clause
*   golang.org/x/net BSD-3-Clause
*   k8s.io/utils Apache-2.0
*   github.com/googleapis/gnostic Apache-2.0
*   github.com/cespare/xxhash/v2 MIT
*   github.com/prometheus/common/internal/bitbucket.org/ww/goautoneg BSD-3-Clause
*   golang.org/x/sys/unix BSD-3-Clause
*   github.com/google/go-cmp/cmp BSD-3-Clause
*   github.com/prometheus/client_golang/prometheus Apache-2.0
*   github.com/beorn7/perks/quantile MIT
*   github.com/prometheus/procfs Apache-2.0
*   golang.org/x/xerrors BSD-3-Clause
*   github.com/google/gofuzz Apache-2.0
*   sigs.k8s.io/cluster-api Apache-2.0
*   sigs.k8s.io/yaml MIT
*   github.com/golang/protobuf BSD-3-Clause
*   github.com/onsi/gomega MIT
*   k8s.io/client-go Apache-2.0
*   github.com/go-openapi/jsonreference Apache-2.0
*   github.com/emicklei/go-restful MIT
*   k8s.io/kube-openapi/pkg Apache-2.0
*   github.com/prometheus/client_model/go Apache-2.0
*   cloud.google.com/go/compute/metadata Apache-2.0
*   github.com/modern-go/concurrent Apache-2.0
*   github.com/google/uuid BSD-3-Clause
*   golang.org/x/text BSD-3-Clause
*   github.com/pkg/errors BSD-2-Clause
*   gomodules.xyz/jsonpatch/v2 Apache-2.0
*   github.com/PuerkitoBio/urlesc BSD-3-Clause
*   github.com/golang/mock/gomock Apache-2.0
*   github.com/docker/distribution Apache-2.0
*   k8s.io/klog Apache-2.0
*   github.com/evanphx/json-patch BSD-3-Clause
*   github.com/matttproud/golang_protobuf_extensions/pbutil Apache-2.0
*   github.com/opencontainers/go-digest Apache-2.0
*   github.com/go-openapi/spec Apache-2.0
*   github.com/metal3-io/cluster-api-provider-metal3 Apache-2.0
*   k8s.io/api Apache-2.0
*   github.com/blang/semver MIT
*   sigs.k8s.io/controller-runtime Apache-2.0
*   golang.org/x/oauth2 BSD-3-Clause
*   github.com/hashicorp/golang-lru MPL-2.0
*   github.com/golang/groupcache/lru Apache-2.0
*   github.com/prometheus/common Apache-2.0
*   github.com/mailru/easyjson MIT
*   github.com/gogo/protobuf BSD-3-Clause
*   github.com/davecgh/go-spew/spew ISC
*   github.com/modern-go/reflect2 Apache-2.0
*   gopkg.in/yaml.v2 Apache-2.0
*   github.com/spf13/pflag BSD-3-Clause
*   k8s.io/apimachinery Apache-2.0
*   golang.org/x/time/rate BSD-3-Clause
*   github.com/metal3-io/baremetal-operator/pkg/apis Apache-2.0
*   github.com/PuerkitoBio/purell BSD-3-Clause
*   k8s.io/cluster-bootstrap/token Apache-2.0
*   golang.org/x/crypto/ssh/terminal BSD-3-Clause
*   github.com/json-iterator/go MIT
*   github.com/imdario/mergo BSD-3-Clause
*   github.com/go-openapi/swag Apache-2.0
*   github.com/go-logr/logr Apache-2.0
*   k8s.io/apiextensions-apiserver/pkg/apis/apiextensions Apache-2.0
*   github.com/go-openapi/jsonpointer Apache-2.0
*   gopkg.in/fsnotify.v1 BSD-3-Clause
*   gopkg.in/inf.v0 BSD-3-Clause
*   golang.org/x/net BSD-3-Clause
*   k8s.io/utils Apache-2.0
*   github.com/googleapis/gnostic Apache-2.0
*   github.com/cespare/xxhash/v2 MIT
*   github.com/prometheus/common/internal/bitbucket.org/ww/goautoneg BSD-3-Clause
*   golang.org/x/sys/unix BSD-3-Clause
*   github.com/google/go-cmp/cmp BSD-3-Clause
*   github.com/prometheus/client_golang/prometheus Apache-2.0
*   github.com/beorn7/perks/quantile MIT
*   github.com/prometheus/procfs Apache-2.0
*   golang.org/x/xerrors BSD-3-Clause
*   github.com/google/gofuzz Apache-2.0
*   sigs.k8s.io/cluster-api Apache-2.0
*   sigs.k8s.io/yaml MIT
*   github.com/golang/protobuf BSD-3-Clause
*   github.com/onsi/gomega MIT
*   k8s.io/client-go Apache-2.0
*   github.com/go-openapi/jsonreference Apache-2.0
*   github.com/emicklei/go-restful MIT
*   k8s.io/kube-openapi/pkg Apache-2.0
*   github.com/prometheus/client_model/go Apache-2.0
*   cloud.google.com/go/compute/metadata Apache-2.0


# Other Considerations


## Cloud Native

**_Does the project meet the definition of Cloud Native?  The CNCF charter states:_**


    _“Cloud native technologies empower organizations to build and run scalable applications in modern, dynamic environments such as public, private, and hybrid clouds. Containers, service meshes, microservices, immutable infrastructure, and declarative APIs exemplify this approach._


    _“These techniques enable loosely coupled systems that are resilient, manageable, and observable. Combined with robust automation, they allow engineers to make high-impact changes frequently and predictably with minimal toil.”_

Metal<sup>3</sup> fits into the Cloud Native ecosystem because:



*   It enables cluster administrators provision bare-metal nodes for both Kubernetes and standalone that enable users to run cloud native applications
*   It’s integrated with Kubernetes which is one of the main enablers for cloud native workloads.


## Project and Code Quality

**_Are there any metrics around code quality?  Are there good examples of code reviews? Are there enforced coding standards?_**


### Code Quality

In the Cluster API provider, the expected code coverage is minimum 80% (except API declaration folder). All code is supposed to have unit tests and some integration tests. In addition we run end to end tests in the CI.

The baremetal-operator also includes unit tests and integration tests. Code coverage from the unit tests is 42%. Increasing this is covered in code review. This component is also exercised heavily by the end-to-end tests


### Code Review

The code review follows the Kubernetes standards, with owner files defined for each project and in a more granular way where needed. All members of the metal3 community have the possibility to use the /lgtm command, but only the approvers and use the /approve command. This ensures that the PR is reviewed by at least two persons. In addition, all jobs in the CI must pass for the PR to be merged, this include unit tests, linting for markdown and shell, gofmt and go vet, and an end to end test in a job that deploys a cluster in a development environment using all pieces of the project.


### Coding Standards

There are some pieces in place related to coding standards, release processes etc. for example: 



*   [https://github.com/metal3-io/cluster-api-provider-metal3/blob/master/CONTRIBUTING.md](https://github.com/metal3-io/cluster-api-provider-metal3/blob/master/CONTRIBUTING.md) 
*   [https://github.com/metal3-io/cluster-api-provider-metal3/blob/master/docs/testing.md](https://github.com/metal3-io/cluster-api-provider-metal3/blob/master/docs/testing.md)
*   [https://github.com/metal3-io/cluster-api-provider-metal3/blob/master/docs/releasing.md](https://github.com/metal3-io/cluster-api-provider-metal3/blob/master/docs/releasing.md) 
*   [https://github.com/metal3-io/baremetal-operator/blob/master/docs/testing.md](https://github.com/metal3-io/baremetal-operator/blob/master/docs/testing.md) 

In those, the points covered are test coverage expectations, code certificate of origin, release process, PR and review process etc.

They also have a process for triage: [https://github.com/metal3-io/metal3-docs/blob/master/processes/triage.md](https://github.com/metal3-io/metal3-docs/blob/master/processes/triage.md) and a process to add new contributors: [https://github.com/metal3-io/metal3-docs/blob/master/maintainers/README.md](https://github.com/metal3-io/metal3-docs/blob/master/maintainers/README.md)

**_What are the performance goals and results? What performance tradeoffs have been made?  What is the resource cost?_**

Metal3 has prioritized a simpler deployment model (a single Deployment) with a smaller overall footprint over massive scale.  We assume provisioning operators can be batched in chunks, so we have not tried to support provisioning of hundreds of nodes at a time or something like that.  This also helps us stay on target for a platform that works well for smaller scale clusters for Edge use cases, as well.

**_What is the CI/CD system?  Are there code coverage metrics?  What types of tests exist?_**

The CI/CD in Metal3 consists of two different units. There is a Prow cluster running in the Packet infrastructure, that performs all unit tests, linting, formatting etc. Then there is a Jenkins setup running in the Nordix infrastructure that performs a variety of end to end tests, deploying clusters in different setups, with different OSes etc. All PRs must pass all Prow jobs and at least one of the Jenkins end to end jobs, depending on which project the PR belongs to.


### Code Coverage

For the unit tests, the agreement for the code coverage in the CAPI provider is minimum 80% on folders other than the API declaration. All functions must be tested and have a unit test function, even in the API declaration folder.

The baremetal-operator also includes unit tests and integration tests.  Code coverage from the unit tests is 42%.  Increasing this is covered in code review.  This component is also exercised heavily by the end-to-end tests.

**_Has a security assessment by the security SIG been done? If not, what is the status/progress of the assessment?_**

No security assessment has been done by SIG security. Not applicable for Sandbox.


# Promotion to Incubation

While Metal<sup>3</sup> is not yet applying to be promoted to the incubation stage, we will provide insights into the progress towards incubation to show the potential of the project.


## Open Governance

**_How are committers chosen? How are architectural and roadmap decisions made? How many decision makers are outside the sponsoring organisation._**

They have a process to elect maintainers : [https://github.com/metal3-io/metal3-docs/blob/master/maintainers/README.md](https://github.com/metal3-io/metal3-docs/blob/master/maintainers/README.md)

The architectural decisions are done through enhancement proposals. The person wishing to propose a new feature / change in design etc. submits a PR against our metal3-docs project, containing a proposal using the defined template: [https://github.com/metal3-io/metal3-docs/blob/master/design/_template.md](https://github.com/metal3-io/metal3-docs/blob/master/design/_template.md). The PR is reviewed and discussed among the community, until a lazy consensus is reached. Not all proposals make it through this process but the dropped proposals usually bring a second proposal that is more consensual among the community, taking into account all feedback of the first proposal.

Regarding the roadmap decisions, they are discussed in the mailing list of the community, and also during the community meetings every other week.

Whether or not belonging to a sponsoring organisation, everybody has the right to submit a proposal with regards to architecture or roadmap. The decision is then taken as a community after discussion. There are some proposals that have been submitted by members outside of a sponsoring organisation (for example Dell EMC).


## Vendor Independence

**_Is the project reasonably independent from the sponsoring vendor? Are all communication channels and project resources hosted just for this project or with other CNCF projects/resources? Is all code that is part of the project hosted and part of the CNCF managed orgs and repos?  Are all defaults for upstream reporting either unset or community hosted infrastructure (i.e. doesn’t point to vendor hosted SaaS control plane or analytics server for usage data)? Is all project naming independent of vendors?  _**

All parts of Metal<sup>3</sup> are provided open-source and are hosted on GitHub. All code is released under the Apache 2.0 license.

**_Relevant Assets regarding vendor independence_**

As mentioned previously all these are the two main components.



*   Metal<sup>3</sup> bare-metal operator: [https://github.com/metal3-io/baremetal-operator](https://github.com/metal3-io/baremetal-operator)
    *   The operator uses [openstack-ironic](https://wiki.openstack.org/wiki/Ironic). This component is open source and [its license](https://opendev.org/openstack/ironic/src/branch/master/LICENSE) is Apache 2.0. A per the CNCF IP policy: “_CNCF project dependencies that are licensed under Apache-2.0 do not require further license review or approval, since they are under the same license as the CNCF project itself.”_
*   Metal<sup>3</sup> cluster API provider:  [https://github.com/metal3-io/cluster-api-provider-metal3](https://github.com/metal3-io/cluster-api-provider-metal3).

The primary language is Golang for those two components and all libraries are open source:



*   [https://github.com/metal3-io/baremetal-operator/blob/master/go.mod](https://github.com/metal3-io/baremetal-operator/blob/master/go.mod)
*   [https://github.com/metal3-io/cluster-api-provider-metal3/blob/master/go.mod](https://github.com/metal3-io/cluster-api-provider-metal3/blob/master/go.mod)


## Successful production usage

**Document that it is being used successfully in production by at least three independent end users which, in the TOC’s judgement, are of adequate quality and scope.**

Metal<sup>3 </sup>is currently being used as a preview in Red Hat’s OpenShift distribution and internally in Ericsson. It is also the foundation for the Airship project led by AT&T.  We expect production deployments of Metal3 this year.


## Healthy number of committers

**Have a healthy number of committers. A committer is defined as someone with the commit bit; i.e., someone who can accept contributions to some or all of the project.**



*   The Metal<sup>3</sup> operator has a total of [39 committers](https://github.com/metal3-io/baremetal-operator/graphs/contributors) and 5 have made significant commits
*   The Metal<sup>3</sup> cluster API provider has [18 committers](https://github.com/metal3-io/cluster-api-provider-metal3) and 7 committers have made significant commits. 


## Substantial ongoing flow of commits

See:



*   For the Metal<sup>3</sup> operator [https://github.com/metal3-io/baremetal-operator/graphs/commit-activity](https://github.com/metal3-io/baremetal-operator/graphs/commit-activity). 3 to 5 weekly commits on average.
*   For the Metal<sup>3</sup> cluster API provider  [https://github.com/metal3-io/cluster-api-provider-metal3/graphs/commit-activity](https://github.com/metal3-io/cluster-api-provider-metal3/graphs/commit-activity). 4 to 5 weekly commits on average.


## A clear versioning schema

The Metal<sup>3</sup> operator component [doesn’t have a clear versioning schema](https://github.com/metal3-io/baremetal-operator/releases) (not a requirement for Sandbox)

The Metal<sup>3 </sup>cluster API component uses the [semver](https://semver.org/) [version schema](https://github.com/metal3-io/cluster-api-provider-metal3/releases)


# SIG-Runtime Review Comments

SIG-Runtime recommends to accept the Metal<sup>3</sup> project into the CNCF:



*   The Metal<sup>3</sup> project fulfills all the formal criteria for Sandbox
*   The Metal<sup>3</sup> fills a gap in the Kubernetes and cloud native ecosystem of provisioning bare metal machines and Kubernetes nodes 

SIG-Runtime also recommend some action items to advance the project further:



*   It is already in the future of Metal<sup>3</sup>’s plans: emphasis on a variety of different production environments.
*   Establish a clear versioning schema for the Metal<sup>3</sup> bare-metal operator.
*   The project has many different components and moving pieces so it would be helpful to establish a mechanism that would allow new end-users to provide feedback on the documentation. This way in the future it could be made easier for first timers to get started which in turn would help wider adoption.
