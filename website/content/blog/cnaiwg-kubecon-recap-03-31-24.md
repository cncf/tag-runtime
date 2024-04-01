# CNAI & Kubecon EU Paris 2024 Recap

Some of the members of the Cloud Native AI Working Group got the chance to attend CloudNativeCon/KubeCon EU 2024 in Paris last week, One of the main topics of the conference centered around AI, how Cloud Native is a key enabler and how AI itself can continue to help Cloud Native and the open source ecosystem. This blog is a recap of some of the conference conversations and our recent publication of the Cloud Native AI Whitepaper. We will follow the same structure that was used in the white paper and fit the discussions and feedback accordingly.

## The Journey of an AI Model

AI, ML, and Data Science are relatively new topics at KubeCon. Although they have been discussed in the past, this year's KubeCon focused on the growing interest in AI/ML. As a result, many of the talks started to address the relationship between the cloud native eco-system and AI/ML

Machine learning has been around for years. Many of the software products we use daily incorporate one or more aspects of machine learning, which is to say that machine learning is not a new paradigm. Still, machine learning was an important guest at this KubeCon, and many of the conversations at Kubecon were centered around the journey of a machine learning model within cloud native.

### AI, ML, Data Science, It’s Just Math!

![CN AI and Data Science Intersection](https://github.com/cncf/tag-runtime/assets/7659560/57a0cca8-3102-4d82-b105-53ba54c83ce4)

AI > ML > Deep Learning. AI is the application of machine learning and deep learning to simulate human intelligence and problem-solving capabilities.  Ultimately, it’s just math! The question is, how does this math find its way to cloud-native, who are the main personas, and what’s the role of each persona? These were all questions we kept getting during Kubecon.

### Interdisciplinary Personas

To level-set, let’s ground our discussion around the traditional machine learning lifecycle which should still apply in the world of Large Language Models (LLMs)  and Generative AI.

The ML lifecycle involves a collaborative effort among various disciplines and roles to ensure machine learning models' successful development, deployment, and maintenance, here are the main personas involved:

- **Data engineers** 
  - **Role**: responsible for data collection, preprocessing, and storage, ensuring that high-quality, reliable data is available for training and inference.
  - **Quotes/Mottos**: “I make data science easier”, “I am the unsung hero that does all the data plumbing, after all bad data in bad data out”
- **Data scientists** 
  - **Role: **define the problem, explore data, select appropriate models/algorithms, train the models, and evaluate model performance. 
  - **Quotes/Mottos:** “I solve business problems”, “I don’t want to learn about infrastructure if I don’t have too”
- **Platform engineers**
  - **Role: **Create scalable and efficient infrastructure, including cloud platforms and distributed computing systems, to support large-scale machine learning workflows. 
  - **Quotes/Mottos: “**I abstract complexity and build APIs to make the lives of data engineers and data scientists easier” 
- **Site reliability engineers (SREs)**
  - **Role: **focus on maintaining system reliability, monitoring performance, and implementing automated processes for deploying and monitoring machine learning models in production. 
  - **Quotes/Mottos: “**I keep it all running 99.99999999% of the time”
- **Hardware architects** 
  - **Role: **contribute by designing and optimizing hardware accelerators, such as GPUs and TPUs, to improve machine learning tasks' computational efficiency and speed. 
  - **Quotes/Mottos:** “I make those models run fast”

This interdisciplinary collaboration to streamline the machine learning lifecycle is described in the following diagram:

![Interdisciplinary Diagram](https://github.com/cncf/tag-runtime/assets/7659560/22e0f39c-eb1c-458a-8c8c-dedcb31471c7)

While not immediately clear, each persona ***connects**** *with other personas at different layers to make the entire lifecycle whole. 

With an understanding of the various layers and how the personas collaborate, we are ready to cover the relationship between Cloud Native and Cloud Native AI.

### The Evolution of the Cloud Native Definition

Cloud native AI represents an evolutionary step in the cloud native paradigm, extending the principles of cloud native computing to artificial intelligence (AI) and machine learning (ML) applications.

It highlights the seamless integration of AI/ML workflows into cloud native environments, leveraging containerization, microservices architecture, and orchestration tools like Kubernetes. Cloud native AI enables organizations to deploy and manage AI/ML models more efficiently, with scalability, agility, and resource optimization benefits. By leveraging cloud native technologies, AI/ML workflows are automated, monitored, and scaled dynamically based on demand, leading to faster development cycles and improved application performance. This evolution aligns with the broader trend of modernizing IT infrastructures and leveraging cloud services to drive innovation and competitiveness in the AI space.

# 

## CNCF Cloud Native AI Working Group

### Why?

The reason we decided to create a cloud native AI working group under the Cloud Native Computing Foundation (CNCF) was to address AI practitioners' growing complexity and challenges in deploying and managing AI/ML workflows in cloud-native environments. The working group aims to raise awareness about common challenges, including but not limited to scalability, interoperability, performance optimization, and security issues.

Additionally, we aim to identify best practices, standards, and approaches to tackle these challenges effectively by bringing together experts from various domains. Moreover, it can facilitate knowledge sharing, collaboration, and the development of tools and frameworks tailored for cloud-native AI applications.

Establishing a common language and framework within the CNCF ecosystem for cloud native AI will simplify the job for AI practitioners, foster innovation, and accelerate the adoption of cloud native technologies in AI and the use of AI in cloud native.

![Four Pillars Diagram](https://github.com/cncf/tag-runtime/assets/7659560/ae39bb24-673d-4061-84be-5a68ef718350)

# 

### Form, Storm, Norm

AI and Machine Learning bring a long list of tools, frameworks, and new terminology. As part of the group’s forming, storming, and norming process, we aim to identify a common language, distill the jargon into concepts and buildings blocks, and build a good understanding of roles, personas, as well as comprehend the relationships between the components and layers of the stack and how each layer affects the others (as shown in the figure below).

![Relationships Diagram](https://github.com/cncf/tag-runtime/assets/7659560/2a87229e-f705-4416-9076-5ec87b1a9a79)

### Perform

Once we understand the ecosystem, the relationships, and the roles, we can start to focus on solving real problems and asking the right questions. During KubeCon, AI was discussed in multiple contexts, here are a few examples:

- What is the impact of AI on sustainability, and how are we going to use cloud-native to build AI/ML applications responsibly?
- What is the impact of cloud native AI on businesses?
- How to evolve the cloud native ecosystem, especially Kubernetes, to address issues around scheduling and batch workloads?
- How to improve inference speed?
- How to evaluate AI/ML applications?
- How to monitor, observe, and signal issues for AI/ML?
- …

All of this is food for thought for the group to ***perform**** *and start drafting best practices and standards on how to tackle each and every one of these questions. Additionally, how do we do so for each of the use cases and industry verticals that plan to use cloud native tooling to build AI/ML applications? Another way of putting it is how do we focus our efforts and the cloud native AI stack to solve real problems. 

![Landscape Focus Picture](https://github.com/cncf/tag-runtime/assets/7659560/3a5b884c-93fc-4db7-80a0-1bfc859e9d1e)

### Initiatives

The Cloud Native AI working group is at the early stages of its initiatives, focusing on several key areas to educate and empower the community in cloud-native AI practices. One of its primary goals is to provide educational resources and guidance to make it easier for newcomers to start with MLOps or AI Engineering, offering workshops, tutorials, and reference implementations as learning tools. The working group plans to develop the Cloud Native AI Landscape and Radar, mapping out different technology verticals and trends in the cloud native AI space.

Collaborating closely with the LF AI & Data Foundation, the group aims to deep dive into specific areas such as training, tuning, and serving AI models, sharing best practices, and fostering innovation. To benchmark performance and promote healthy competition, the working group intends to establish the Cloud Native AI Model leaderboard. Event planning and open collaboration with the community are also key priorities, with a willingness to consider and incorporate suggestions to further enhance its initiatives and impact in the cloud native AI ecosystem.

#### Initiatives Summary

- Educate the community
- Make it easy to start with MLOps or AI Eng
- Workshop
- Reference implementation(s)
- CN AI Landscape
- CN AI Radar (different tech verticals)
- Collaborate with the LF AI & Data
- Deep dive into different areas. i.e. training, tuning, serving
- CN AI Model leaderboard (performance)
- Event planning
- Open to suggestions!

## Final Thoughts

We are incredibly excited about the potential and opportunities ahead in the Cloud Native AI Working Group and the broader Cloud Native AI space. With a strong focus on education, collaboration, and innovation, we anticipate significant advancements in cloud native AI practices, making it more accessible and efficient for practitioners and organizations. The initiatives planned, such as workshops, reference implementations, AI model leaderboards, and collaboration with organizations like the LF AI & Data, are poised to drive meaningful progress and create a vibrant ecosystem of solutions.

We look forward to the contributions, partnerships, and insights that will emerge, ultimately leading to transformative developments and breakthroughs in AI applications and technologies.
