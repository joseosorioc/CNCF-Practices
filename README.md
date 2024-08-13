# CNCF-Practices
Practices and study of Kubernetes  inside linux fundation
Kubernetes and Cloud Native Associate 


<h2>What is Cloud Native?</h2>

Cloud native is the software approach of building, deploying, and managing modern applications in cloud computing environments. Modern companies want to build highly scalable, flexible, and resilient applications that they can update quickly to meet customer demands. To do so, they use modern tools and techniques that inherently support application development on cloud infrastructure. These cloud-native technologies support fast and frequent changes to applications without impacting service delivery, providing adopters with an innovative, competitive advantage.
How does a cloud-native approach benefit businesses?
Organizations gain competitive advantages in various ways when they build cloud-native software applications.

Increase efficiency

Cloud-native development brings along agile practices like DevOps and continuous delivery (CD). Developers use automated tools, cloud services, and modern design culture to build scalable applications rapidly.

Reduce cost

By adopting the cloud-native approach, companies don't have to invest in the procurement and maintenance of costly physical infrastructure. This results in long-term savings in operational expenditure. The cost savings of building cloud-native solutions might also benefit your clients.

Ensure availability

Cloud-native technology allows companies to build resilient and highly available applications. Feature updates do not cause downtime and companies can scale up app resources during peak seasons to provide a positive customer experience. 
What are cloud-native applications?
Cloud-native applications are software programs that consist of multiple small, interdependent services called microservices. Traditionally, developers built monolithic applications with a single block structure containing all the required functionalities. By using the cloud-native approach, software developers break the functionalities into smaller microservices. This makes cloud-native applications more agile as these microservices work independently and take minimal computing resources to run. 



Variations y Cloud Native: Public, Private, Hybrid





Benefits - Application in Cloud Native





Cloud Native Philosophies

Important: 

- The Linux Foundation is founded in 2000. 
- Kubernetes is Open Source





Cloud Native Architecture Fundamentals - Further Study

Characteristics of Cloud Native Applications

Cloud Native Applications harness the power of the cloud to provide increased resilience, agility, operability, and observability. Let's dive a bit deeper into these characteristics.

Resiliency

Resilient applications are designed to withstand failures and continue to function or recover quickly. They typically make use of patterns such as redundancy, failover, and graceful degradation. Self-healing, where systems automatically detect and recover from failure, is a key aspect of resilient cloud-native applications. Kubernetes, for instance, has a built-in self-healing mechanism where it maintains a desired number of pod replicas and replaces failed instances.

Agility

Agility in the context of cloud-native applications refers to the ability to quickly build, modify, and deploy applications. Agile practices such as microservices and continuous delivery pipelines, backed by automation, promote rapid iteration and responsiveness to change.

Operability

Operability encompasses the ease of deploying, running, and managing applications. Cloud-native applications are designed to be easily monitored, configured, and maintained. They typically leverage automation and Infrastructure as Code (IaC) tools like Terraform to streamline operations and minimise toil.

Observability

Observability is the ability to understand the internal state of your system based on the outputs it generates. It's a critical component in diagnosing issues and understanding how an application behaves in the wild. Logging, monitoring, and tracing (collectively known as the 'three pillars of observability') are vital practices to understand the state and performance of cloud-native applications.

It is important as part of your studies especially if you’re planning on taking the KCNA exam to remember these characteristics! A friendly anagram for this is “RAOO: Racoons are Often Observant” -

Racoons Are Often Observant = Resiliency, Agility, Operability, Observability



Tips:

For the KCNA Examination, concentrate on the following aspects:

IAC - Understand the meaning of Infrastructure as Code and its connection to Cloud Native principles
The roles of Speed, Efficiency, and Cost in the context of Cloud Native environments






<h4>Cloud Native Architecture Fundamentals - Further Study</h4>

Key Pillars of Cloud Native Architecture

Building upon the characteristics and practices discussed, cloud-native architecture is sometimes referenced as being founded on four key pillars:

1. <strong>Microservices Architecture</strong>

Microservices architecture involves breaking down the application into loosely coupled, independently deployable components, each focusing on a single responsibility. This design enables agility, scalability, and resilience as each microservice can be developed, scaled, and managed independently.

2.  <strong>Containerisation</strong> 

Containerisation involves encapsulating an application with its dependencies into a container, which can run uniformly across different environments. It facilitates isolation, consistency, and efficiency, making applications easier to build, deploy, and manage.

3.  <strong>DevOps</strong> 

DevOps is a collaborative approach that combines software development (Dev) and IT operations (Ops) to enhance the efficiency, reliability, and speed of software delivery. By fostering a culture of excellence, DevOps emphasises automation, monitoring, and collaboration across development and operations teams.

4.  <strong>Continuous Delivery (CD)</strong>  

Continuous Delivery is a practice where code changes are automatically built, tested, and prepared for a release to production. CD accelerates the release cycle, enhances productivity, and reduces the risk, complexity, and downtime of application deployment.

In essence, building cloud-native applications is a strategy that promotes agility, resilience, operability, and observability by leveraging modern technological practices.




<h2>AutoScaling</h2>

What Is Auto-scaling?
Auto-scaling is a scaling technique you can apply to workloads hosted in a cloud environment. One of the major benefits of cloud-based hosting is that you can readily scale capacity to whatever extent is needed to support the demand for your service. Auto-scaling takes that advantage a step further. With auto-scaling, as the demand for a given workload changes over time, the amount of resources allocated to support that workload adapts automatically to meet your performance requirements.

Before auto-scaling was an option, scaling workloads was often challenging. Allocating resources manually to support a workload is inherently error-prone because it is difficult to precisely predict changes in demand or know how many resources are needed to handle those changes. This ambiguity can lead to costly over-provisioning on the one hand, or potential service disruptions due to under-provisioning on the other. Auto-scaling helps solve these problems by automatically increasing or decreasing the amount of resources assigned to your workload in direct proportion to the amount that demand also increases or decreases.

In this article, we’ll cover how auto-scaling works, why it is important, and when organizations are likely to use it. We’ll also look at the most common offerings for auto-scaling, along with potential challenges that accompany its implementation. Finally, we’ll discuss some important considerations for implementing an auto-scaling architecture effectively.

How Does Auto-scaling Work?
To understand auto-scaling, you should first consider that two types of scaling are possible:

Scaling out/horizontal scaling
With horizontal scaling, you increase or decrease the number of nodes (or Kubernetes pods) participating in a given workload. An advantage of horizontal scaling is that it allows you to add a virtually unlimited amount of new capacity without affecting existing nodes or creating downtime. Compared to vertical scaling, it’s also a faster method of scaling capacity. However, not every application or workload can be scaled horizontally.

Scaling up/vertical scaling
This type of scaling increases or decreases the available memory and/or processing power for existing nodes. For example, you can vertically scale two server nodes provisioned with 16 GB of RAM and 4 vCPUs to have 64 GB of RAM and 16 vCPUs apiece. In some cases, such as with relational databases that have been implemented without any sharding, vertical scaling has the advantage of being the only viable way to scale in response to increased demand.

However, a key downside of vertical scaling is that it does not lend itself as well to automation as horizontal scaling does.

This article will generally focus on horizontal auto-scaling, as that is what is typically used in automated scaling scenarios. (Teams are more likely to handle vertical scaling manually.)

When Does Auto-scaling Occur?
With auto-scaling, you typically configure resources to scale automatically in response to an event or metric threshold chosen by your organization. Engineers identify these events and metric thresholds as ones that most closely correlate with degraded performance.

For example, a developer could create a threshold of 70 percent memory usage for greater than four minutes. The developer could then additionally configure a response that would launch two additional instances every time this threshold is met or crossed. The developer could also define a minimum and maximum limit for scaling. What is the minimum acceptable number of nodes that should ever be used to run this workload, and conversely, what is the maximum?

Graphic identifying an auto-scaling group with minimum size, current capacity, scale-out capacity, and maximum size.Auto-scaling groups can be configured with a minimum and maximum limit for scaling.
Besides relying on triggering events or metrics, you can also configure auto-scaling to occur according to a predetermined schedule. For companies and services that have cyclical (or otherwise predictable) load demands, this method lets you preemptively scale infrastructure in anticipation of higher demand and then scale back as needed.


<h2>AutoScaling types</h2>

Reactive Autoscaling
![image](https://github.com/user-attachments/assets/cda9633d-3b2c-49b8-a095-8bc4a346821f)


Scheduler Autoscaling (can plan ahead to avoid latency disruption )
![image](https://github.com/user-attachments/assets/b8409631-c9d6-4a17-8ba0-0ae8770dde0d)

Predictive autoscaling (Intelligent autoscaling)
![image](https://github.com/user-attachments/assets/3e368566-eaf8-496d-9a0a-4bab12930eb0)

<h3>Kubernetes Autoscaling</h3>

Cluster Autoscaler

![image](https://github.com/user-attachments/assets/e2a8d755-09c8-400b-a64c-a057d5361380)

KEDA

![image](https://github.com/user-attachments/assets/15a49480-c865-4727-a174-19bb36e80e59)

Horizontal and verticual pod Autoscaler

![image](https://github.com/user-attachments/assets/58a4f934-bbbe-4c17-8fc4-a49bc7abc95f)


<h2>Important:</h2>

Horizontal Pod AutoScaler: scales the number of replicas of an application </br>

Vertical Pod AutoScaler: VPA scales the resource requests and limits of a pod


As you prepare for the KCNA exam, the following video will cover crucial topics that require your particular attention -

The definition and rationale behind adopting the Serverless pattern in Cloud Native architectures
The concept of CloudEvents, including their significance and impact within Cloud Native ecosystems

<h2>Serverless</h2>

Serverless is Event Driven Architecure. 
![image](https://github.com/user-attachments/assets/eadf21b4-3a50-4b5f-8414-1c8d95b02c0b)


Serverless Scale Infinitely
![image](https://github.com/user-attachments/assets/ea4f77ec-74bd-4ead-9351-78151040a7ca)



Cloud Native Serverless tool

![image](https://github.com/user-attachments/assets/5b821b3e-004a-4b31-a84a-77fca6523635)

What is Scale to Zero?
The concept is pretty simple. Your serverless resources are automatically and dynamically scaled to zero when they are not in use. This means that you only pay for the resources you use. And no surprise performance spikes when your resources are scaled up.

<h3>Cloud Events especification</h3>

Events are everywhere. However, event producers tend to describe events differently.

The lack of a common way of describing events means developers must constantly re-learn how to consume events. This also limits the potential for libraries, tooling and infrastructure to aide the delivery of event data across environments, like SDKs, event routers or tracing systems. The portability and productivity we can achieve from event data is hindered overall.

CloudEvents is a specification for describing event data in common formats to provide interoperability across services, platforms and systems.

CloudEvents has received a large amount of industry interest, ranging from major cloud providers to popular SaaS companies. CloudEvents is hosted by the Cloud Native Computing Foundation (CNCF) and was approved as a Cloud Native sandbox level project on May 15, 2018, an incubator project on Oct 24, 2019 and a graduated project on Jan 25, 2024 (announcement).

![image](https://github.com/user-attachments/assets/da3c49d1-c4b4-44b4-8b94-97e2580b237f)


![image](https://github.com/user-attachments/assets/9e907525-ca4f-4040-8b6e-da4af7291005)


What is the scaling model referred to as when using Serverless and its event-driven architecture?
- Scale to zero

- What does provisioned concurrency in Serverless offerings refer to?
- The number of instances that can be run simultaneously

- What is a possible disadvantage of using Serverless architecture?
It may incur latency during periods where the application is less active

How can CloudEvents be used according to the CloudEvents specification?
Agnostically across various services, platforms, and systems

How does Serverless architecture handle concurrency?
It typically manages concurrency as part of the offering

Which feature of Serverless offerings helps manage the workload and billing?
Budget thresholds

Which two aspects of Serverless computing are critical to understand from a cost perspective?
- code execution and autoscaling

- What is one of the challenges posed by Serverless solutions from a Cloud Native viewpoint?
- They may lead to vendor lock-in due to lack of standardised APIs

- What is the scaling model referred to as when using Serverless and its event-driven architecture?
- scale to zero


<h2>Knative</h2>

Knative is an Open-Source Enterprise-level solution to build Serverless and Event Driven Applications. Serverless refers to running back-end programs and processes in the cloud. Serverless works on an as-used basis, meaning that companies only use what they pay for. Knative is a platform-agnostic solution for running serverless deployments.

![image](https://github.com/user-attachments/assets/75a92e61-5b17-47da-94a8-0f9c001a1025)


Opinion reddit member (keda vs serverless)

When I discuss "serverless" developers everyone gets very excited by "scale to zero" as a differentiator to running pods on Kubernetes.

My take on this is:

Production rarely needs to scale to zero. In fact with Lambda I have seen hacks where period requests are sent to actually prevent it for latency reasons.

Non-production it's really handy to scale down because otherwise such environments are just burning money.

So ideally what we really want is to "scale down to near zero". This comes built in with Kubernetes HPA and newer tools like Keda. But in my experience devs are afraid to enable them....

So my recommendation is embrace autoscaling! Be brave or use tools where its baked in and you don't have to worry about the choice 


<h3>Community and Governance</h3>

Community and Governance - Study Tips
As you embark on your journey to excel in the KCNA exam, the following video will cover topics that require your particular attention -

- How is conflict resolution handled in the various CNCF groups
- What is the meaning of the different acronyms commonly used
- What is the core role of the CNCF TOC

<h4>CNCF Mission</h4>

Our charter
“CNCF’s mission is to make cloud native computing ubiquitous…”

Cloud Native terminology

CNCF Chams diagram

![image](https://github.com/user-attachments/assets/d20312d5-a6dc-405d-be17-460f30ce8802)


![image](https://github.com/user-attachments/assets/7045624b-e67a-422c-b110-d7086b4c9118)

![image](https://github.com/user-attachments/assets/e52a3048-a3cc-4cf3-92f1-c94f1109b808)


Stages Projects CNCF

![image](https://github.com/user-attachments/assets/34451f8b-e507-4e2c-9db9-b1aa2d89a2fe)


Project Graduation CNCF

![image](https://github.com/user-attachments/assets/74e01857-6577-4def-bdf5-42fea62ae40a)

