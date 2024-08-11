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
