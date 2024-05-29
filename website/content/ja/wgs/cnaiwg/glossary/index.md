---
title: 用語集
toc_hide: false
list_pages: true
weight: 4
---

Defines key terms used in the Cloud Native Working Group’s writings.

See also: [CNCF Glossary](https://glossary.cncf.io/)

## LLM

 "LLM" stands for "Large Language Model." Large language models are artificial intelligence models trained on vast amounts of text data to understand and generate human-like text. LLMs are a subset of machine learning models specifically designed for natural language processing (NLP) tasks.

## MLOps

MLOps, short for machine learning operations, refers to the practices, methodologies, and tools used to streamline and automate machine learning models' deployment, monitoring, and management in production environments. MLOps aims to bridge the gap between machine learning development and operations, ensuring that ML models are deployed efficiently, reliably, and at scale. It involves a combination of software engineering principles, DevOps practices, and specialized tools to automate the end-to-end ML lifecycle, including data preparation, model training, model deployment, monitoring, and maintenance. MLOps helps organizations accelerate their ML projects, improve model performance, and maintain consistency and reliability across the ML pipeline.

## LLMOps

LLMOps, which stands for Large Language Model Operations, encompasses the operational aspects tailored specifically for Large Language Models (LLMs). In essence, LLMOps is the adaptation of MLOps principles and tools to the unique requirements of LLM-powered applications, encompassing their entire lifecycle from development to deployment and maintenance.

## vGPU

vGPU, or Virtual Graphics Processing Unit, technology enables multiple virtual machines (VMs) to share a single physical GPU (Graphics Processing Unit). This technology efficiently utilizes GPU resources in virtualized environments such as cloud computing, data centers, and virtual desktop infrastructure (VDI).

## MIG

Multi-Instance GPU technology is an innovation that allows a single physical GPU (Graphics Processing Unit) to be partitioned into multiple more minor instances, each operating as an independent GPU with its own resources and capabilities. This technology enhances GPU utilization and flexibility in data center and cloud computing environments.

## MPS

MPS stands for Multi-Process Service in the context of GPU computing. MPS technology allows multiple GPU-accelerated applications or processes to share a single physical GPU while maintaining isolation and efficient resource utilization.

## DRA

DRA stands for Dynamic Resource Allocation. It is an API abstraction of general resource claim and provisioning for Pods, allowing 3rd party vendors to provide HW/SW resources on demand without having to rewrite the Kubernetes core API.

## RAG

In the context of AI, RAG stands for "Retrieval-Augmented Generation." It's a model architecture combining retrieval-based and generative models to produce text.

RAG's generation process is augmented with a retrieval mechanism that helps the model access relevant information from an extensive database or knowledge base. This retrieval component allows the model to incorporate external knowledge into the generation process, improving the quality and relevance of the generated text.

## AI Practitioners

In the context of this paper, it refers to (not limited to) ML Engineers, Data Scientists, Data Engineers, roles whose primary responsibilities include manipulating relevant data, creating, and optimizing machine learning models.

## Developers

In the context of this paper, it refers to (not limited to), Software Engineers, Frontend Engineers, Backend Engineers, Full Stack Engineers, Software Architects, and Software Testers. The roles whose primary responsibility include writing and testing software including user interfaces, microservices, and backend software.

## Deployers

In the context of this paper, it refers to (not limited to), DevOps Engineers, Site Reliability Engineers, Infrastructure Engineers, Infrastructure Architects, Application Administrators, Cluster Administrators. The roles whose primary responsibility include deploying software and cloud infrastructure to multiple environments including development, staging and production.

## Data engineers

- **Role**: Responsible for data collection, preprocessing, and storage, ensuring that high-quality, reliable data is available for training and inference.
- **Quotes/Mottos**: “I make data science easier”, “I am the unsung hero that does all the data plumbing, after all bad data in bad data out”

## Data scientists

- **Role**: define the problem, explore data, select appropriate models/algorithms, train the models, and evaluate model performance.
- **Quotes/Mottos**: “I solve business problems”, “I don’t want to learn about infrastructure if I don’t have too”

## Platform engineers

- **Role**: Create scalable and efficient infrastructure to support large-scale machine learning workflows, including cloud platforms and distributed computing systems.
- **Quotes/Mottos**: “I abstract complexity and build APIs to make the lives of data engineers and data scientists easier”

## Site reliability engineers

- **Role**: focus on maintaining system reliability, monitoring performance, and implementing automated processes for deploying and monitoring machine learning models in production.
- **Quotes/Mottos**: “I keep it all running 99.99999999% of the time”

## Hardware architects

- **Role**: contribute by designing and optimizing hardware accelerators, such as GPUs and TPUs, to improve machine learning tasks’ computational efficiency and speed.
- **Quotes/Mottos**: “I make those models run fast”
