---
title: "Kubernetes and AI: 5 Talks You don't want to Miss at KubeCon India 2024"
date: 2024-012-06
author: Sudhanshu Prajapati
---

KubeCon + CloudNativeCon started in 2016 and is hosted by the Cloud Native Computing Foundation (CNCF), a subsidiary of the Linux Foundation. This conference brings together technologists and adopters from the open source and cloud native communities to exchange insights and explore trends. Over the years, it has been held in various countries and cities ([KubeCon North America 2024](https://kccncna2024.sched.com/), [KubeCon Europe 2024](https://kccnceu2024.sched.com/)). However, for the first time, it will take place in India, right in the heart of the capital, New Delhi. As India’s inaugural KubeCon + CloudNativeCon, the event is set to welcome over 3,000 of the most talented professionals in the industry. This makes it an exceptional opportunity to connect with industry leaders and learn from top cloud native experts. If you haven’t registered yet, don’t wait—head over to the [registration](https://events.linuxfoundation.org/kubecon-cloudnativecon-india/register/#kubecon-cloudnativecon-india-rates) page!

As part of the CNCF ecosystem, the [WG-AI Working Group](https://tag-runtime.cncf.io/wgs/cnaiwg/charter/) under the Cloud Native [TAG Runtime](https://tag-runtime.cncf.io/) is at the forefront of enabling artificial intelligence in cloud-native environments. The group's mission is to empower the community by providing best practices, frameworks, and tools to streamline AI adoption. With a strong focus on raising awareness, fostering innovative approaches, simplifying workflows, and establishing a common language for AI integration, WG-AI is making AI more accessible and actionable for cloud-native practitioners.

**How to Get Involved:**

* **Community Meetings**: Held every Second & Fourth Friday, 8 AM - 9 AM PT
* **Slack Channel**: Connect with the group on CNCF Slack in the `#wg-artificial-intelligence` channel.

For more details and additional resources, refer to the [WG-AI Charter](https://tag-runtime.cncf.io/wgs/cnaiwg/charter/).

The purpose of this blog is to guide AI/ML enthusiasts in navigating the exciting talks at KubeCon/CloudNativeCon. We’ve curated five must-attend sessions that highlight the intersection of AI/ML and cloud-native technologies. So, without further ado, let’s dive in!

>***Disclaimer: The slides and videos for these talks have not yet been published, so the information provided here is based solely on the title and abstract of each session.***

## Talks

* Multi-Node Finetuning LLMs on Kubernetes: A Practitioner’s Guide [[Link to talk](https://kccncind2024.sched.com/event/9dbde73800fce96e47fc6acadcdbf76a)]

    This session is for those interested in fine-tuning and training models on multi-node GPU infrastructure and understanding what it takes to get such systems up and running. It delves into the technologies behind it, like PyTorch FSDP—Fully Shared Data Parallel—which scales AI model training using a Distributed Data-Parallel technique. Here, each process or worker handles a batch of data, and FSDP enables data parallelism by sharding model parameters, allowing distributed training with a smaller GPU footprint. Beyond these techniques, you'll learn why GPU Direct RDMA is critical for achieving peak performance. This talk offers a practical guide loaded with valuable insights.

* Trust in Green: Towards a Cloud Native Approach for Building Sustainable and Reliable Enterprise AI [[Link to talk](https://kccncind2024.sched.com/event/47fe873b4686380f3302ae8f8b56875e)]

    This session is for those who want to build efficient and scalable AI systems in cloud-native environments. It explores the collaborative efforts of CNCF AI WG and TAG Environmental Sustainability to create a repeatable design approach that optimizes compute resources, storage, and networking for AI workloads. With a focus on reducing unnecessary resource consumption and ensuring resilience and scalability, the session offers actionable strategies to deploy AI systems that are not only high-performing but also mindful of resource efficiency. Attendees will leave with practical insights to streamline their AI/ML lifecycle and future-proof their deployments.

* From CPU to GPU: Progressive Delivery for Complex ML Deployments [[Link to talk](https://kccncind2024.sched.com/event/951651bf94b13deef1c7faf2a054b9af)]

    Nowadays, when we talk about traditional CPU workload pipelines, i.e., application deployment, we roughly know how the CI/CD pipeline will look. In addition to that, there are many CI/CD tools available in the cloud-native landscape to help us achieve this. However, when it comes to ML CI/CD, the universe as we know it changes. New replicas can take up to an hour to become operational due to extended image pull times. How can one achieve progressive delivery for these ML deployments? This is where this talk helps, offering real-world lessons from designing CI/CD pipelines for GenAI applications. This is a must-attend talk for anyone looking to understand the nuances of designing efficient progressive delivery for multi-resource deployments.

* GenAI Recipes For Cloud Native Deployment [[Link to talk](https://kccncind2024.sched.com/event/3436292649f6f06728c99adc60a8ee23)]

    This talk is helpful for anyone looking to understand and implement Generative AI (GenAI) applications in cloud-native environments. It offers practical insights into using OPEA, a flexible framework for building GenAI systems with components like LLMs, data stores, and prompt engines. Attendees will learn how to deploy these systems across various hyperscalers, explore architectural blueprints for Retrieval-Augmented Generation (RAG) workflows, and review real-world scale testing results with over 50K documents. Whether you're exploring enterprise AI or optimizing existing workflows, this session provides actionable knowledge and a clear path to adopting and contributing to OPEA.

* Optimizing 5G Networks: Deploying AI/ML Workloads with the AIMLFW of O-RAN SC [[Link to talk](https://kccncind2024.sched.com/event/b0772d54f4c6986f481c0f9d7873f937)]

    This session is for anyone curious about how AI/ML frameworks are reshaping 5G network management within the O-RAN Software Community (O-RAN SC). It provides an accessible introduction to O-RAN’s mission and architecture before diving into real-world AI/ML use cases, such as traffic prediction and anomaly detection, showcasing how these solutions scale with AIMLFW.

## What’s next?

If you’re excited to explore more about cloud-native AI/ML, now is the perfect time to engage with the **WG-AI Working Group**. This vibrant community brings together experts and enthusiasts working to integrate AI seamlessly within cloud-native ecosystems. Some of the group members may even be attending KubeCon + CloudNativeCon India this year—an excellent opportunity to meet them in person and discover how you can get involved. To find out who to reach out to and learn more, engage with the group on CNCF Slack in the **#wg-artificial-intelligence** channel. Regular community meetings are held every **Second & Fourth Friday, 8 AM - 9 AM PT**, offering a great way to stay updated and contribute. For more resources and detailed information, check out the [WG-AI Charter](https://tag-runtime.cncf.io/wgs/cnaiwg/charter/).