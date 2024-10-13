---
title: Glossary
toc_hide: false
list_pages: true
weight: 4
---

Defines key terms used in the Cloud Native Working Group’s writings.

See also: [CNCF Glossary](https://glossary.cncf.io/)

## AI for Cloud Native (AI for CN)

A set of frameworks, concepts, and tools that use of AI in Cloud Native environments to improve and extend the functionality of infrastructure management. These include, agent actions, actionable advice, assistants, as well as AI platforms for managing CN systems.

## Cloud Native for AI (CN for AI)

A class of techniques and solutions that enable AI developers and deployers to effectively develop, deploy, run, scale, and monitor their AI workloads on cloud infrastructure. Effectively can mean better performance, lower cost, simplified usage, etc.

## Cloud Native Artificial Intelligence (CNAI)

Cloud Native Artificial Intelligence (CNAI) refers to approaches and patterns for building and deploying AI applications and workloads using the principles of Cloud Native.  Enabling repeatable and scalable AI-focused workflows allows AI practitioners to focus on their domain.

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

## Personas in the Cloud Native AI Landscape

### Data Engineers

* **Role:** Handle data collection, preprocessing, and storage, ensuring high-quality, reliable data for training and inference.
* **Quotes/Mottos:**
  * "I make data science easier."
  * "I'm the unsung hero that does all the data plumbing – after all, bad data in, bad data out."

### AI Engineers

* **Role:** Handle model selection, fine-tuning, and integration of AI components into larger systems.
* **Quotes/Mottos:**
  * "I build the brains behind the applications."
  * "I make sure the models are accurate and efficient."

### AI Application Developers (Coders)

* **Role:** Focus on developing AI applications and using AI to improve existing applications.
* **Quotes/Mottos:**
  * "I bring AI to life in real-world applications."
  * "I'm building the future of software with AI."

### Platform Engineers

* **Role:** Create and maintain an Internal Developer Platform to improve developer productivity. They help organizations enforce security and compliance through automated pipelines and help developers find and connect to pre-approved AI models and APIs.
* **Quotes/Mottos:**
  * "I empower developers to build and deploy faster and safer."
  * "I'm the architect of the developer experience."


### Security Architect/Engineer

* **Role:** Focus on protecting AI systems from threats and vulnerabilities. Implement measures to safeguard data, models, and infrastructure.
* **Quotes/Mottos:**
  * "I'm the guardian of AI security."
  * "I make sure AI systems are safe and trustworthy."

### AI Ethicists

* **Role:** Ensure responsible AI practices, particularly in design and deployment stages.
* **Quotes/Mottos:**
  * "I advocate for ethical AI development and deployment."
  * "I ensure AI benefits humanity."

### Compliance Officers

* **Role:** Ensure AI systems comply with regulations and governance standards.
* **Quotes/Mottos:**
  * "I navigate the legal and regulatory landscape of AI."
  * "I make sure AI systems are compliant and responsible."

### Prompt Engineers

* **Role:** Specialize in crafting effective prompts for generative AI models.
* **Quotes/Mottos:**
  * "I speak the language of AI."
  * "I unlock the creative potential of language models."

### AI Safety Researchers

* **Role:** Focus on ensuring the safety and ethical implications of generative AI models.
* **Quotes/Mottos:**
  * "I build guardrails for responsible AI."
  * "I ensure AI remains beneficial to humanity."

### MLOps Engineers

* **Role:** Focus on the operationalization of machine learning models.
* **Quotes/Mottos:**
  * "I bridge the gap between models and production."
  * "I ensure machine learning models are ready for the real world."

### AI Product Managers

* **Role:** Oversee the development of AI products from conception to launch.
* **Quotes/Mottos:**
  * "I guide AI products from idea to impact."
  * "I ensure our AI solutions meet market needs."

### AI Researchers

* **Role:** Explore AI techniques that may not be immediately applicable to products.
* **Quotes/Mottos:**
  * "I push the boundaries of what AI can do."
  * "I explore today what will be mainstream AI tomorrow."

### Data Scientists

* **Role:** Define the problem, explore data, select appropriate models/algorithms, train models, and evaluate model performance.
* **Quotes/Mottos:**
  * "I solve business problems."
  * "I don't want to learn about infrastructure if I don't have to.""

### Site Reliability Engineers

* **Role:** Focus on maintaining system reliability, monitoring performance, and implementing automated processes for deploying and monitoring machine learning models in production.
* **Quotes/Mottos:** "I keep it all running 99.99999999% of the time."

### Hardware Architects

* **Role:** Design and optimize hardware accelerators (e.g., GPUs and TPUs) to improve machine learning tasks' computational efficiency and speed.
* **Quotes/Mottos:** "I make those models run fast."