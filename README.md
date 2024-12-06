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


¿Qué es el almacenamiento en la nube?
El almacenamiento en la nube es un modelo de computación en la nube que permite almacenar datos y archivos en Internet a través de un proveedor de computación en la nube, al cual se accede mediante la red pública de Internet o una conexión de red privada dedicada. El proveedor almacena, administra y mantiene de manera segura los servidores de almacenamiento, la infraestructura y la red para garantizar que tiene acceso a los datos cuando lo necesite, prácticamente a cualquier escala y con capacidad elástica. El almacenamiento en la nube hace que ya no sea necesario comprar y administrar su propia infraestructura de almacenamiento de datos, lo que le brinda agilidad, escalabilidad y durabilidad, con acceso a los datos en cualquier momento y lugar. Ejemplos de Cloud Storage es EBS, EFS. El cloud Storage es importante en Cloud Native.

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

1. The "Crossing the Chasm" concept in the CNCF project maturity model represents which transition?
- From Incubated to Graduated

The "Chasm" phase in the CNCF Project Maturity levels represents the bridge to which user category?
- Early Majority

What is the role of the Technical Oversight Committee (TOC) in the CNCF?
-  To evaluate the maturity of CNCF projects.

What is the significance of Sandbox, Incubation, and Graduation stages in the CNCF?
- They signal the level of maturity of a given project to enterprises.

What was the change in CNCF's terminology to avoid confusion with other projects?
- SIG to TAG

How is conflict resolution generally handled within CNCF governance?
- Through discussion and voting

What is the significance of the CNCF Landscape page?
- It provides an overview of the ecosystem of cloud native projects, including those in Sandbox, Incubated, and Graduated stages

Which group, according to the "Crossing the Chasm" model, is most susceptible to risk and will wait for market adoption to increase before utilizing a project themselves?
Late Majority

Important Study in the context CNCF
- Early Adopters
- Early Majority
- Late Majority
- Laggards

![image](https://github.com/user-attachments/assets/d20312d5-a6dc-405d-be17-460f30ce8802)


![image](https://github.com/user-attachments/assets/7045624b-e67a-422c-b110-d7086b4c9118)

![image](https://github.com/user-attachments/assets/e52a3048-a3cc-4cf3-92f1-c94f1109b808)


Stages Projects CNCF

![image](https://github.com/user-attachments/assets/34451f8b-e507-4e2c-9db9-b1aa2d89a2fe)


Project Graduation CNCF

![image](https://github.com/user-attachments/assets/74e01857-6577-4def-bdf5-42fea62ae40a)




CNCF Personas

Understand and recognise the acronyms commonly associated with the role of SRE, i.e. SLA, SLO and SLI
Understand the role of SRE and how this differs to DevOps
The role of FinOps for financial accountability



Open Standards

We have: 

- Open Container Initiative: The Open Container Initiative (OCI) is a lightweight, open governance structure (project), formed under the auspices of the Linux Foundation, for the express purpose of creating open industry standards around container formats and runtimes. The OCI was launched on June 22nd 2015 by Docker, CoreOS and other leaders in the container industry.
The OCI currently contains three specifications: the Runtime Specification (runtime-spec), the Image Specification (image-spec) and the Distribution Specification (distribution-spec). The Runtime Specification outlines how to run a "filesystem bundle" that is unpacked on disk. At a high-level an OCI implementation would download an OCI Image then unpack that image into an OCI Runtime filesystem bundle. At this point the OCI Runtime Bundle would be run by an OCI Runtime.

![image](https://github.com/user-attachments/assets/568c3a93-93b3-48d8-8332-5435397c5ad0)


![image](https://github.com/user-attachments/assets/c8c88cf5-90c8-4d45-9738-7ffb24ff292e)



- Container Network Interface: 
CNI (Container Network Interface), a Cloud Native Computing Foundation project, consists of a specification and libraries for writing plugins to configure network interfaces in Linux and Windows containers, along with a number of supported plugins. CNI concerns itself only with network connectivity of containers and removing allocated resources when the container is deleted. Because of this focus, CNI has a wide range of support and the specification is simple to implement. Se centra en el Networking.

![image](https://github.com/user-attachments/assets/81d3627b-57fe-48b6-aa1e-17bc1d2d0601)


- Container Storage Interface
Introduction
Container Storage Interface (CSI) is an initiative to unify the storage interface of Container Orchestrator Systems (COs) like Kubernetes, Mesos, Docker swarm, cloud foundry, etc. combined with storage vendors like Ceph, Portworx, NetApp etc. This means, implementing a single CSI for a storage vendor is guaranteed to work with all COs.

Projects graduateds and comercial

![image](https://github.com/user-attachments/assets/cdc4679a-d29d-4a29-9b08-8345ba06e15a)

![image](https://github.com/user-attachments/assets/9c88f85a-cf45-4577-b46e-f6d38bf82a3e)


A standard interface for service meshes on Kubernetes.

Service Mesh Interface provides:

- A standard interface for service meshes on Kubernetes.
- A basic feature set for the most common service mesh use cases.
- Flexibility to support new service mesh capabilities over time.
- Space for the ecosystem to innovate with service mesh technology.
- 


<h4>Contenerisation introduction </h4>

Chroot: Chroot, short for "change root," is a Unix command that alters the apparent root directory for a specific process and its children. It creates a confined environment, isolating processes from the rest of the system. This isolation can be handy for various purposes, such as testing and debugging or enhancing security.

What was Docker originally called? 
- DotCloud

What are the two key ingredients that Docker brought together to create its solution?
- Linux namespaces and cgroups

Why are Docker containers preferred over virtual machines?
- They are faster to deploy and consume less system resources

How many namespaces were originally added to the Linux kernel in 2002?
- 6

What is the network namespace in Linux used for?
- To provide an isolated networking stack with its own IP addresses and connectivity

What is the purpose of the mount namespace in Linux?
To allow the use of independent mount points that are visible by processes within the namespace.


<h3> Docker Desktop Configuration </h3>
What does Docker Desktop use to run an isolated instance for Docker?
- A hidden virtual machine or "subsystem".

What is the purpose of the "i" flag when running the 'docker run' command?
- To make the container interactive

What is the purpose of the "t" flag when running the 'docker run' command?
- To create a terminal input/output environment (tty) for interacting with the container

What is one key difference between managing resources in Docker Desktop on a Mac compared to Windows?
- On a Mac, you can customise shared resources in the Preferences, while on Windows, you cannot


<h3> Container Images </h3>

Difference Container vs Images

![image](https://github.com/user-attachments/assets/bba307fd-94a6-4ee4-8141-2925489eb0a4)


Container tags
![image](https://github.com/user-attachments/assets/ba051c69-272e-472a-aff0-876f5869af88)


What  the digest?
![image](https://github.com/user-attachments/assets/fe969881-7597-4df1-9bba-940ae363ad76)
Digest se refiere a un identificador único que representa de manera inmutable el contenido de una imagen. Es una forma de garantizar la integridad y la exactitud de una imagen a lo largo del tiempo.

What is the purpose of the "latest" tag in Docker?
To indicate the newest version of a container image

What is a union filesystem in the context of container images?
A filesystem that combines individual layers into a single view

What is the difference between a digest and an image ID?
A digest is a checksum taken from a container registry, while an image ID is a checksum based on the local container image

<h4>Images containers part #2 </h4>

What is the command used to validate the Docker version and configuration?
- docker version

** What is the container engine being used by Docker?
- containerD

** What is the purpose of the -rm option when running a Docker container?
- To remove the container if exists

What command, in the original Docker command syntax, would display all containers, irrespective of their state, including those that have exited?
- DOcker ps -a

** How can you override the default command in a Docker container when running it? - ¿Cómo se puede anular el comando predeterminado en un contenedor Docker al ejecutarlo?
Add the command to the end of the docker run command

** What does the it option do when running a Docker container?
Runs the container in interactive mode with a terminal

** Which command line option is used to list all the parameters available to the Docker command?
docker --help

** What is the purpose of running a container as a non-root user?
To improve security by limiting privileges

Importante: Glosario de Terminos en Kubernetes: https://kubernetes.io/es/docs/reference/glossary/?fundamental=true

Cloud Storage o Almacenamiento en la nube


<h3>Container Networking Services and Volumes</h3>

El comando docker <strong>run -d --rm nginx </strong> ejecuta un contenedor de Docker con la imagen de Nginx de la siguiente manera:

docker run: Este es el comando básico para ejecutar un contenedor Docker.
-d: Esta opción ejecuta el contenedor en modo "desprendido" o "detached", lo que significa que el contenedor se ejecutará en segundo plano y no bloqueará tu terminal.
--rm: Esta opción indica que el contenedor debe eliminarse automáticamente cuando se detenga. Es útil para mantener limpio tu entorno de Docker, ya que evita la acumulación de contenedores detenidos.

nginx: Es la imagen de Docker que se utilizará para crear el contenedor. En este caso, se está usando la imagen oficial de Nginx, que es un servidor web popular.

docker ps: Este comando muestra una lista de los contenedores que están actualmente en ejecución. Solo muestra aquellos que están activos en ese momento, es decir, aquellos cuyo estado es "Up" (en funcionamiento).


docker ps -a: Este comando muestra una lista de todos los contenedores, tanto los que están en ejecución como los que están detenidos. Incluye contenedores que han sido detenidos, terminados o que han fallado.

docker rm:

Propósito: Elimina contenedores Docker.
Uso: Se utiliza para borrar uno o más contenedores que ya han sido detenidos. No se puede usar para eliminar contenedores que están en ejecución.
Sintaxis: docker rm [OPTIONS] CONTAINER [CONTAINER...]
Ejemplo: docker rm my_container elimina el contenedor llamado my_container.


docker rmi:

Propósito: Elimina imágenes Docker.
Uso: Se utiliza para borrar una o más imágenes de Docker del sistema. Las imágenes que están en uso por contenedores en ejecución no se pueden eliminar a menos que se detengan los contenedores que las utilizan.
Sintaxis: docker rmi [OPTIONS] IMAGE [IMAGE...]
Ejemplo: docker rmi my_image elimina la imagen llamada my_image.

<img width="967" alt="Captura de pantalla 2024-09-02 a la(s) 11 41 57 p  m" src="https://github.com/user-attachments/assets/70b574b2-fa47-4673-bf61-f19e418d2e80">
 <i>el comando docker stop se utiliza para detener contenedores en ejecución.</i>

docker stop

Propósito: Detener uno o más contenedores que están en ejecución.
Uso: Envía una señal de SIGTERM al proceso principal dentro del contenedor, dándole la oportunidad de terminar de manera ordenada. Si el proceso no termina dentro de un tiempo de espera (por defecto, 10 segundos), se envía una señal SIGKILL para forzar la detención del contenedor.

docker exec

Ejecuta un comando en un contenedor en ejecución.
Ejemplo: docker exec -it my_container /bin/bash


-P (En mayuscula)

El comando -P (o --publish-all) se usa con el comando docker run para exponer todos los puertos expuestos de un contenedor a puertos disponibles en el host. Aquí está cómo funciona:

docker run -P
Propósito: Exponer todos los puertos que la imagen del contenedor ha definido como expuestos (EXPOSE en el Dockerfile) y asignar puertos aleatorios disponibles en el host para cada uno de ellos.
Uso: Cuando usas -P, Docker asigna automáticamente un puerto en el host para cada puerto expuesto del contenedor. La asignación es automática y no necesitas especificar un puerto específico.
Ejemplo de Uso: docker run -d -P nginx
Luego, para hacer mas interesante el ejercicio podemos hacer curl sobre eso: curl http://localhost:55000



docker exec -it ef1 bash

El comando docker exec -it ef1 bash se utiliza para ejecutar un nuevo proceso dentro de un contenedor Docker en ejecución. Aquí está el desglose del comando:

docker exec: Este es el comando principal para ejecutar un nuevo comando en un contenedor que ya está en ejecución.

-i: Esta opción significa "modo interactivo". Mantiene la entrada estándar (stdin) abierta, lo que permite interactuar con el proceso que se está ejecutando.

-t: Esta opción asigna un pseudo-terminal al proceso, lo que es necesario para una experiencia interactiva adecuada (como tener una terminal de línea de comandos).

ef1: Este es el ID o nombre del contenedor en el que deseas ejecutar el comando. Puedes usar el ID completo del contenedor o su nombre.

bash: Este es el comando que se ejecutará dentro del contenedor. En este caso, se está ejecutando el intérprete de comandos bash, lo que te proporciona una línea de comandos dentro del contenedor.



El comando docker run -d --rm -p 12345:80 se utiliza para ejecutar un contenedor Docker con las siguientes opciones:

docker run: Este es el comando principal para crear y ejecutar un nuevo contenedor a partir de una imagen Docker.

-d (Deteached): Esta opción ejecuta el contenedor en modo "desprendido" (detached), lo que significa que el contenedor se ejecutará en segundo plano y no bloqueará tu terminal.

--rm: Esta opción indica que el contenedor debe eliminarse automáticamente una vez que se detenga. Esto ayuda a mantener limpio tu entorno Docker al eliminar contenedores que ya no están en uso.

-p 12345:80: Esta opción mapea el puerto 80 del contenedor al puerto 12345 del host. Específicamente:

El primer número (12345) es el puerto en el host.
El segundo número (80) es el puerto dentro del contenedor.




El comando <strong>docker run -d --rm -p 12345:80 nginx -v my_web_page:/usr/share/nginx/html nginx</strong> 

Análisis del Comando
docker run -d --rm -p 12345:80 nginx: Esta parte del comando está bien y se utiliza para ejecutar un contenedor Nginx en segundo plano (-d), eliminar el contenedor automáticamente al detenerse (--rm), y mapear el puerto 80 del contenedor al puerto 12345 del host (-p 12345:80).

-v my_web_page:/usr/share/nginx/html: Esta opción se usa para montar un volumen desde el host al contenedor.

nginx: Aparece nuevamente al final del comando, pero debería estar antes de las opciones del contenedor. El nombre de la imagen que vamos a usar.




docker start

El comando docker start se utiliza para iniciar uno o más contenedores que están detenidos. Aquí está un desglose del comando y su uso:

docker start
Propósito: Inicia uno o más contenedores que están en estado detenido. No crea nuevos contenedores, sino que reinicia contenedores existentes que ya han sido creados anteriormente.

Uso: Este comando es útil cuando necesitas reactivar un contenedor que fue detenido pero aún existe en el sistema.

Sintaxis: docker start [OPTIONS] CONTAINER [CONTAINER...]

CONTAINER: El ID del contenedor o el nombre del contenedor que deseas iniciar. Puedes proporcionar uno o varios IDs o nombres de contenedores.


BUILDING Docker Images

FROM: Especifica la imagen padre de la cual vamos a construir. 
![image](https://github.com/user-attachments/assets/2113426c-21b8-43d7-8dd1-a35a2e44d6bd)

*** ANTES se USABA MAINTAINER:  MAINTAINER John Doe <john.doe@example.com> Pero quedo descontinuada, ahora se usa LABEL maintainer="John Doe <john.doe@example.com>"


APK  (Alpine Package Kepper)

![image](https://github.com/user-attachments/assets/a963b0ff-790f-44cf-965d-3163b811f00d)

Querying the termininfo database

![image](https://github.com/user-attachments/assets/b05f3248-cad1-47fc-bb14-7303e3556f92)


RUN
En Docker, la instrucción RUN en un Dockerfile se utiliza para ejecutar comandos en el contenedor durante el proceso de construcción de la imagen. Es una de las instrucciones más importantes y versátiles en un Dockerfile.
![image](https://github.com/user-attachments/assets/d42a5253-df62-46ab-972e-6a464e08638c)


CMD

La cláusula CMD en un Dockerfile se utiliza para especificar el comando que se ejecutará por defecto cuando se inicie un contenedor a partir de la imagen construida. Es decir, define qué proceso debe ejecutarse cuando el contenedor se ejecuta sin que se especifique un comando diferente en la línea de comandos de docker run.
![image](https://github.com/user-attachments/assets/c2515880-e5e1-42ac-bdb8-fced920ac5b4)


WORKDIR

La cláusula WORKDIR en un Dockerfile se utiliza para establecer el directorio de trabajo para cualquier comando RUN, CMD, ENTRYPOINT, COPY y ADD que aparezca después de esta instrucción. Es una forma de configurar el directorio en el que se ejecutan los comandos dentro del contenedor, proporcionando un entorno organizado y consistente para la construcción de la imagen.

![image](https://github.com/user-attachments/assets/6c7cff32-35d1-4159-aa50-413eed1712b9)


COPY
La cláusula COPY en un Dockerfile se utiliza para copiar archivos y directorios desde el contexto de construcción (el directorio en el que se encuentra el Dockerfile) al sistema de archivos del contenedor en construcción.


USER

La cláusula USER en un Dockerfile se utiliza para especificar el usuario y el grupo con el que se ejecutarán los comandos en el contenedor a partir de ese punto en el Dockerfile. Establecer un usuario específico es importante por razones de seguridad y para garantizar que las aplicaciones se ejecuten con los permisos adecuados.

![image](https://github.com/user-attachments/assets/b29c3524-6b76-4451-b31d-11b41be7aa04)

WHOAMI (NO es necesariamente de dockerfile, sino de UNIX)
whoami, es un comando en sistemas Unix/Linux que muestra el nombre del usuario actual. Sin embargo, en el contexto de Docker, hace referencia a cómo obtener información sobre el usuario que está ejecutando comandos dentro de un contenedor.


ENTRYPOINT
La instrucción ENTRYPOINT en un Dockerfile define el comando que se ejecutará por defecto cuando se inicie un contenedor a partir de la imagen construida. A diferencia de CMD, que proporciona comandos predeterminados que pueden ser sobrescritos, ENTRYPOINT establece UN (uno solo) comando principal que no puede ser sobrescrito fácilmente al iniciar el contenedor, aunque puedes pasarle argumentos adicionales.
![image](https://github.com/user-attachments/assets/53ecc941-4beb-42e9-b304-9f2412f04292)

Importante: 

La opción --no-cache se utiliza con el comando docker build para evitar el uso de cachés durante la construcción de una imagen. Esto significa que Docker no utilizará capas previamente almacenadas en caché para las instrucciones del Dockerfile, sino que volverá a ejecutar cada comando desde cero.

docker system prune: El comando docker system prune en Docker se utiliza para limpiar recursos no utilizados en tu entorno Docker. Esto incluye imágenes, contenedores, volúmenes y redes que no están en uso, ayudando a liberar espacio en disco y mantener tu sistema Docker ordenado.


** What is the difference between the CMD and RUN instructions in a Dockerfile?
  CMD specifies the command that will be executed when the container runs, while RUN executes commands during the build process.
** What is the purpose of a multistage build in a Dockerfile?
 To reduce the size of the final container image

 **In a multistage Dockerfile, how can you copy a binary from one stage to another?
 By using the COPY directive with the --from flag

 ** What is the function of the Logical AND operator (&&) in a Dockerfile?
 To run multiple commands in sequence, only if the previous command is successful







Docker Buildx

Docker Buildx es una extensión del comando docker build que proporciona capacidades avanzadas de construcción de imágenes Docker. Está basado en BuildKit, una herramienta de construcción de imágenes de Docker más moderna y poderosa. Docker Buildx permite crear imágenes de manera más eficiente y flexible, y soporta una serie de características avanzadas que no están disponibles con el comando docker build tradicional.

Características Clave de Docker Buildx
Construcción Multi-Plataforma: Permite construir imágenes para múltiples plataformas (como linux/amd64, linux/arm64, etc.) desde un solo Dockerfile. Esto es útil para crear imágenes que se puedan ejecutar en diferentes arquitecturas de hardware.

Optimización de Caché: Utiliza caché de construcción de forma más eficiente, lo que puede acelerar las construcciones repetidas. Buildx también admite el uso de cachés remotos.

Construcción Paralela: Puede construir múltiples imágenes o etapas de construcción en paralelo, lo que mejora el tiempo de construcción.

Construcción de Imágenes Sin Etiqueta (BuildKit): Permite construir imágenes sin tener que etiquetarlas explícitamente, y manejar construcciones más complejas con mayores niveles de control.

Soporte para Contextos de Construcción: Facilita la construcción de imágenes a partir de diferentes contextos, permitiendo una mayor flexibilidad en la organización de archivos y directorios.

Construcción desde un Dockerfile Multietapa: Maneja construcciones basadas en Dockerfiles que utilizan múltiples etapas, permitiendo una construcción más limpia y modular.


<h2> Container Orchestration - Study Tips </h2>
For the KCNA Examination, understand the problems that Container Orchestration resolves.

![image](https://github.com/user-attachments/assets/3807972b-3223-4700-aeee-0e08cdd09c7e)


CRD (Custom resource definitions) en Kubernetes

Custom resource definitions (CRDs) in Kubernetes are a way to extend its API, allowing us to add functionality and capabilities beyond the basic features provided out of the box.

🌐 Kubernetes has the potential to do much more than its current capabilities, and further extensions are required to unlock its full potential.
  Installing third-party solutions in Kubernetes often involves extending the cluster with custom resource definitions, enabling users to define how certain actions or 
   resources are created and managed.

   En Kubernetes, un CRD, o Custom Resource Definition (Definición de Recurso Personalizado), es una manera de extender el conjunto de recursos que Kubernetes puede manejar de forma nativa. Los recursos personalizados permiten a los usuarios definir sus propios tipos de recursos y objetos en el clúster, además de los recursos predefinidos como Pods, Services y Deployments.

Aquí tienes un desglose básico de cómo funciona un CRD:

Definición del CRD: Primero, defines el CRD en un archivo YAML que describe el nuevo tipo de recurso. Esto incluye especificar el nombre del recurso, su esquema y cómo se debe comportar. Por ejemplo, podrías definir un recurso llamado MyCustomResource con ciertos campos y validaciones.

Creación del CRD: Aplicar este archivo al clúster de Kubernetes crea el CRD, que ahora es reconocido por Kubernetes como un tipo de recurso válido.

Uso del Recurso Personalizado: Una vez que el CRD está en el clúster, puedes crear instancias del nuevo recurso personalizado. Estas instancias son objetos que siguen el esquema definido en el CRD. Puedes interactuar con ellos de la misma manera que con otros recursos de Kubernetes, usando kubectl u otras herramientas.

Controladores: A menudo, se utiliza un controlador para manejar el ciclo de vida de los recursos personalizados. Este controlador es un componente que observa los recursos personalizados y realiza acciones en respuesta a cambios en su estado, similar a cómo los controladores manejan otros recursos en Kubernetes.

Un ejemplo práctico de un CRD podría ser un recurso llamado Database, que tiene campos como databaseName, version, y replicas. Puedes usar este recurso para definir y gestionar instancias de bases de datos en tu clúster.

En resumen, los CRDs permiten a los usuarios de Kubernetes extender la API del clúster para soportar sus propios tipos de datos y aplicaciones personalizadas.


Explicado:  Imagina que Kubernetes es como una gran caja de herramientas para manejar aplicaciones. Las herramientas que vienen con Kubernetes son cosas como “cajas” (Pods) y “tablones de madera” (Services).

Un CRD, o Definición de Recurso Personalizado, es como cuando tú quieres usar una herramienta especial que no está en la caja de herramientas original. Entonces, le dices a Kubernetes: “Quiero usar una nueva herramienta que llamaremos ‘SuperCaja’”.

Así que creas una definición de cómo debe ser esta “SuperCaja” y se la das a Kubernetes. Ahora, Kubernetes sabe qué es una “SuperCaja” y puede usarla junto con las herramientas que ya tiene.

Así, con los CRDs, puedes crear tus propias herramientas personalizadas para hacer cosas especiales en tu clúster de Kubernetes.


Concepto de Open Shift
Open Shift esta basado en Kubernetes, puesto que expanding Kubernetes to have functionality outside of core functionality.

Self-Healing
El término self-healing (autocuración) se refiere a la capacidad del sistema para detectar y corregir problemas automáticamente sin intervención manual.

In the context of Container Orchestration, what is the purpose of 'self-healing'?
- Automatically fixing or replacing containers when they fail.


<h3>Important</h3>

Kubernetes Architecture - Study Tips
For the KCNA Examination it is important to have a thorough understanding of the Kubernetes Architecture and the roles of specific components. When watching the next video pay particular attention to the following areas.

- The role of the kubelet and how it interacts with the CRI (Container Runtime Interface)
- The role of the kube-scheduler
- The role of the kube-proxy
- The role of the kubeapi-server
- The role of etcd
- Container Runtimes and the differences between high level and low level runtimes
- The hierarchy of Kubernetes components - From Cluster to Node to Pod to Container
- What is the CCM (Cloud Controller Manager) and where this would reside in a Kubernetes cluster


Kubernetes Infraestructure

Container Runtime

A bajo nivel: 

Low Level Container Runtime
![image](https://github.com/user-attachments/assets/56aa2e14-bccc-4984-a06f-ebbf163f3351)

RUNC
Open Container Initiative (OCI): runc is the reference implementation of the OCI Runtime Specification, which defines how to run containers on a Linux system.
Functionality: runc is responsible for the actual process of creating and running containers. It takes a container configuration (specified in a JSON format defined by the OCI) and uses Linux system calls to set up the container's environment and then run the container's main process. This involves configuring namespaces, cgroups, security features, and other isolation mechanisms provided by the Linux kernel.


A Alto nivel: 
![image](https://github.com/user-attachments/assets/54a06a46-f748-474f-836b-e0e6196a28cb)


The Kubelet

The kubelet is the primary "node agent" that runs on each node. It can register the node with the apiserver using one of: the hostname; a flag to override the hostname; or specific logic for a cloud provider.

The kubelet works in terms of a PodSpec. A PodSpec is a YAML or JSON object that describes a pod. The kubelet takes a set of PodSpecs that are provided through various mechanisms (primarily through the apiserver) and ensures that the containers described in those PodSpecs are running and healthy. The kubelet doesn't manage containers which were not created by Kubernetes.

Other than from a PodSpec from the apiserver, there are two ways that a container manifest can be provided to the kubelet.

File: Path passed as a flag on the command line. Files under this path will be monitored periodically for updates. The monitoring period is 20s by default and is configurable via a flag.
HTTP endpoint: HTTP endpoint passed as a parameter on the command line. This endpoint is checked every 20 seconds (also configurable with a flag).
kubelet [flags]

Respuesta de brayan bautista: Kubelet
Nos permite interactuar con kubernetes, actua como un demonio o daemond. Habla con los compoenentes del control plane. Habla con containerDI de docker.  Es un agente que se despliega en cada uno de los nodos del cluster y esta en constante comunicacion con el control plane. 


*** Cuando pregunten si Kubelet se ejecuta en un solo nodo del cluster, se ejecuta en ambos:
Respuesta de The Linux Fundation: 

I agree that the documentation's ambiguous description of the kubelet node agent does not quite clarify its purpose.
Both kubelet and kube-proxy node agents are found on every node of the cluster, that includes control-plane node(s) and worker nodes. One of kubelet's tasks is to coordinate with the container runtime the container lifecycle events: to start, stop, delete... Since the control-plane agents (api server, scheduler, controller-manager, etcd) are in fact containers, it is easy to see the need for a kubelet agent on a control-plane node as well.


Statics Pods o pods estaticos

En el contexto de Kubernetes, los "pods estáticos" se refieren a pods que no son gestionados por controladores como Deployments, ReplicaSets o StatefulSets, sino que son gestionados directamente por el plano de control (control plane) de Kubernetes. Estos pods suelen ser utilizados para componentes críticos del sistema, como el servidor API de Kubernetes, el scheduler o el controller manager.

Static Pods are managed directly by the kubelet daemon on a specific node, without the API server observing them. Unlike Pods that are managed by the control plane (for example, a Deployment); instead, the kubelet watches each static Pod (and restarts it if it fails).

Static Pods are always bound to one Kubelet on a specific node.
The kubelet automatically tries to create a mirror Pod on the Kubernetes API server for each static Pod. This means that the Pods running on a node are visible on the API server, but cannot be controlled from there. The Pod names will be suffixed with the node hostname with a leading hyphen.

ETCD
Base de datos llave-valor. Es el cerebro critico de Kubernetes, si este elemento se elimina se borra todo el cluster. Guarda todo el estado del cluster.  Todo lo que ocurra en el cluster (si eliminamos un pod, si lo reiniciamos lo va a registrar )

![image](https://github.com/user-attachments/assets/588a323f-1cbc-438f-b7ae-26810fc93638)

KubeAPI Server

kube api-server: kubernetes expone una API para poder hablar con el cluster. Nos podemos conectar por una api o por una libreria o servicios externos etc.

![image](https://github.com/user-attachments/assets/398380a5-9beb-4e62-9b10-9d0afdf7f843)


Kubectl

Kubectl se comunica directamente con el api-server.


EL SHED o KubeScheduler
Se encarga de buscar donde los pods pueden correr. Es el responsable de definir donde desplegamos los pods.
In Kubernetes, scheduling refers to making sure that Pods are matched to Nodes so that Kubelet can run them.
kube-scheduler is the default scheduler for Kubernetes and runs as part of the control plane. kube-scheduler is designed so that, if you want and need to, you can write your own scheduling component and use that instead.

Kube-scheduler selects an optimal node to run newly created or not yet scheduled (unscheduled) pods. Since containers in pods - and pods themselves - can have different requirements, the scheduler filters out any nodes that don't meet a Pod's specific scheduling needs. Alternatively, the API lets you specify a node for a Pod when you create it, but this is unusual and is only done in special cases.



![image](https://github.com/user-attachments/assets/06dd14d5-acdd-4614-99e1-9e64e564c0b2)


Kube Proxy

Es el encargado de gestionar quien entra y quien sale a nivel de networking. Crea las reglas, quita las reglas etc. Por debajo trabaja con IP tables.

The Kubernetes network proxy runs on each node. This reflects services as defined in the Kubernetes API on each node and can do simple TCP, UDP, and SCTP stream forwarding or round robin TCP, UDP, and SCTP forwarding across a set of backends. Service cluster IPs and ports are currently found through Docker-links-compatible environment variables specifying ports opened by the service proxy. There is an optional addon that provides cluster DNS for these cluster IPs. The user must create a service with the apiserver API to configure the proxy.


Kube DNS
Puede correr en el control plane o en los worker nodes. Es un servicio que no es obligatorio para que kubernetes funcione. Kube DNS es un servidor de DNS. Se encarga de hacer una direccion de dominio, ademas que lo hace automatico.



Core DNS en Kubernetes

CoreDNS es un servidor DNS que actúa como el proveedor de servicios de nombres de dominio (DNS) dentro de un clúster de Kubernetes. Es una parte fundamental del plano de control de Kubernetes y se encarga de resolver nombres de servicio en el clúster a direcciones IP y de proporcionar resolución de nombres para los pods y servicios en el clúster.

Aquí están algunos aspectos clave de CoreDNS en Kubernetes:

Función en Kubernetes:

Resolución de Servicios: CoreDNS se encarga de traducir los nombres de los servicios de Kubernetes (por ejemplo, my-service.default.svc.cluster.local) en direcciones IP de los pods asociados. Esto permite a los pods comunicarse entre sí utilizando nombres de servicio en lugar de direcciones IP, lo que simplifica la configuración y mejora la flexibilidad.
Resolución de Nombres de Dominio Externos: CoreDNS también puede configurarse para resolver nombres de dominio externos (por ejemplo, sitios web en Internet) mediante la reenvío de solicitudes a servidores DNS externos.
Configuración:

CoreDNS se ejecuta como un conjunto de pods en el espacio de nombres kube-system y se gestiona mediante un Deployment en Kubernetes.
La configuración de CoreDNS se realiza a través de un ConfigMap llamado coredns en el espacio de nombres kube-system. Este ConfigMap contiene el archivo de configuración de CoreDNS (generalmente llamado Corefile), que define cómo se deben resolver las solicitudes de DNS.
Características y Beneficios:

Flexibilidad: CoreDNS es altamente configurable y soporta una variedad de plugins que permiten personalizar cómo se resuelven las consultas DNS.
Desempeño: Está diseñado para ser ligero y rápido, lo que ayuda a mantener un buen desempeño en la resolución de nombres dentro del clúster.
Extensibilidad: Ofrece una arquitectura de plugins que permite añadir funcionalidades adicionales como cacheo, balanceo de carga, y más.
Comparación con kube-dns:

Antes de CoreDNS, Kubernetes usaba kube-dns como el proveedor DNS predeterminado. CoreDNS fue adoptado en versiones más recientes de Kubernetes como el reemplazo de kube-dns debido a su mayor flexibilidad y rendimiento.
Diagnóstico y Resolución de Problemas:

Si hay problemas con la resolución DNS en un clúster de Kubernetes, es posible que se deban verificar los logs de los pods de CoreDNS, revisar el archivo Corefile para asegurarse de que la configuración es correcta y usar herramientas de diagnóstico como nslookup o dig para probar la resolución de nombres dentro del clúster.
En resumen, CoreDNS es un componente crítico para la resolución de nombres dentro de un clúster de Kubernetes, facilitando la comunicación entre servicios y proporcionando resolución de nombres tanto para servicios internos como externos.

Core DNS y Kube DNS

CoreDNS y kube-dns son ambos servidores DNS utilizados en Kubernetes, pero no son exactamente lo mismo. Aquí te explico las diferencias clave:

kube-dns
Componentes:

kube-dns es una solución más antigua que se basa en varios componentes:
DNSmasq: Un caché de DNS.
kube-dns: Un componente que se encarga de la resolución de nombres dentro del clúster y de algunos servicios adicionales.
La arquitectura de kube-dns incluye un kube-dns pod que se comunica con DNSmasq para resolver las consultas de DNS.
Configuración:

La configuración se realiza a través de un ConfigMap llamado kube-dns en el espacio de nombres kube-system.
Limitaciones:

kube-dns tiene una arquitectura más compleja debido a la combinación de kube-dns y DNSmasq, y puede ser menos flexible en términos de personalización en comparación con CoreDNS.
CoreDNS
Componentes:

![image](https://github.com/user-attachments/assets/82925c0a-0a4a-4582-b5ad-599ae2968d51)

CoreDNS es una solución más moderna y ligera. Se basa en un solo binario y está diseñado con una arquitectura de plugins que permite una configuración más flexible.
CoreDNS es una implementación de DNS escrita en Go que proporciona características avanzadas y personalizables a través de plugins.
Configuración:

La configuración se realiza a través de un ConfigMap llamado coredns en el espacio de nombres kube-system, que contiene el archivo Corefile. Este archivo permite una configuración modular y extensible.
Ventajas:

Simplicidad: CoreDNS tiene una arquitectura más simple y un solo binario, lo que facilita su gestión y despliegue.
Flexibilidad: CoreDNS ofrece una arquitectura de plugins que permite añadir funcionalidades adicionales como caché, balanceo de carga, y reglas personalizadas.
Desempeño: Está diseñado para ser rápido y eficiente, lo que ayuda a mantener un buen desempeño en la resolución de nombres.
Migración de kube-dns a CoreDNS
Transición: En versiones más recientes de Kubernetes, CoreDNS ha reemplazado a kube-dns como el proveedor de DNS predeterminado. La migración a CoreDNS se realizó debido a su mayor flexibilidad, desempeño y simplicidad en comparación con kube-dns.

Compatibilidad: Aunque CoreDNS es ahora el estándar, Kubernetes sigue soportando kube-dns en clústeres existentes, pero la mayoría de las nuevas instalaciones y actualizaciones prefieren CoreDNS.

Resumen
kube-dns: Más antiguo, basado en múltiples componentes (kube-dns y DNSmasq), con una configuración menos flexible.
CoreDNS: Más moderno, basado en una arquitectura de plugins única, con mayor flexibilidad y simplicidad en la configuración.

Kubernetes usa CoreDNS como el servidor DNS predeterminado a partir de Kubernetes 1.11. CoreDNS se ha convertido en el reemplazo recomendado para kube-dns, que era el servidor DNS utilizado anteriormente.

Leer documento: https://coredns.io/2018/11/27/cluster-dns-coredns-vs-kube-dns/


Kube Controller Manager

Es como un robot en kubernetes que se encarga de controlar todo, si necesitamos eliminar un configmap o un secreto, el se encarga de gestionar esa orden, un deployment esta fallando el se encarga de realizar todas las tareas operativas del cluster.

The Kubernetes controller manager is a daemon that embeds the core control loops shipped with Kubernetes. In applications of robotics and automation, a control loop is a non-terminating loop that regulates the state of the system. In Kubernetes, a controller is a control loop that watches the shared state of the cluster through the apiserver and makes changes attempting to move the current state towards the desired state. Examples of controllers that ship with Kubernetes today are the replication controller, endpoints controller, namespace controller, and serviceaccounts controller.

![image](https://github.com/user-attachments/assets/21ae2844-d26c-4bfc-b8b4-320598b4c99a)



The cloud controller manager

Cloud infrastructure technologies let you run Kubernetes on public, private, and hybrid clouds. Kubernetes believes in automated, API-driven infrastructure without tight coupling between components.

The cloud-controller-manager is a Kubernetes control plane component that embeds cloud-specific control logic. The cloud controller manager lets you link your cluster into your cloud provider's API, and separates out the components that interact with that cloud platform from components that only interact with your cluster.
By decoupling the interoperability logic between Kubernetes and the underlying cloud infrastructure, the cloud-controller-manager component enables cloud providers to release features at a different pace compared to the main Kubernetes project.

The cloud-controller-manager is structured using a plugin mechanism that allows different cloud providers to integrate their platforms with Kubernetes.

Design Kubernetes components

The cloud controller manager runs in the control plane as a replicated set of processes (usually, these are containers in Pods). Each cloud-controller-manager implements multiple controllers in a single process.
![image](https://github.com/user-attachments/assets/904de9fb-488c-432e-a95e-8ec92ab95fdb)


Diferencia entre kube controller Manager y Cloud Controller Manager

The cloud controller manager would then be responsible for running controllers whose function is specific to cloud provider functionality. The kube controller manager would then be responsible for running all controllers whose function was not related to a cloud provider.

Interesante: ETCD se basa en RAFT Concensus, que es un algoritmo. Para leer mas: https://raft.github.io/

Relación entre etcd y Raft
etcd y Raft: etcd utiliza el algoritmo Raft para lograr consenso y mantener la consistencia en su base de datos distribuida. Raft garantiza que todas las instancias de etcd en el clúster estén sincronizadas y tengan la misma información.

Operación de etcd: Cuando un cliente realiza una operación en etcd, como una escritura o una actualización de configuración, el líder de etcd usa Raft para coordinar la escritura y replicarla a los seguidores. Esto asegura que los datos se mantengan consistentes en todas las instancias de etcd, incluso si algunos nodos fallan.


<h3>Kubernetes Architecture Final</h3>
![image](https://github.com/user-attachments/assets/782f09e9-41c2-4c38-8cbb-0f9916fbd51b)

![image](https://github.com/user-attachments/assets/cf4cbd5e-eebf-4b1c-b66b-76396ca67c20)

Questions

Which component is responsible for spawning and running containers in a Kubernetes architecture?
- Low-Level Container Runtime

What is the function of the Kube-Scheduler in the Kubernetes architecture?
- It determines which Nodes are valid placements for Pods according to constraints and resources

What role does the Kube-Proxy play in the Kubernetes infrastructure?
- It dynamically configures TCP/UDP and SCT Forwarding on the system that it runs

What is the role of the Controller-Manager in the Kubernetes architecture?
- It is a control loop that monitors the state of your cluster and makes or requests changes.

Which component bridges functionality of the cloud provider to the Kubernetes server?
- Cloud-Controller-Manager

What protocol is used by distributed systems to ensure that each node in the cluster agrees on the same state even in the face of failures?
- RAFT (Es el algoritmo raft)

How do nodes in a highly available Kubernetes configuration connect to the API server?
- They connect via the loadbalancer

Which of the following correctly represents the hierarchy of Kubernetes components, from broadest to most specific?
- Cluster -> Node -> Pod -> Container

When does the Kubernetes Kube-Scheduler determine the node placement for a pod? ***
- After the pod has been created and registered in ETCD

If a Kubernetes cluster hosted on a public cloud provider fails to provision a requested load balancer service, which component might be responsible for this failure?
- The Cloud-Controller-Manager

Which of the following is considered a component of the Kubernetes control-plane?
- Cloud-Controller-Manager

How do nodes in a highly available Kubernetes configuration connect to the API server?
- They connect via the loadbalancer


<h3>Kubernetes Pods - Study Tips</h3>

This topic was split into three owing to the many areas that we also need to cover for the KCNA examination as niche questions. When watching these chapters, pay particular attention to the following topics -

What is a pod
How to create pods (both via the CLI and with YAML)
How to access documentation related to a pod specification (kubectl explain)
How to execute a command in a running pod (kubectl exec)
Pod restart policies (the default value and available options)
The difference between Declarative and Imperative approaches when using kubectl
How pods make use of the network namespace for a shared IP address
How pods are able to communicate without the use of NAT or other complicated network setups
Running multiple containers in a pod
Accessing logs from a particular container when running multiple containers in a pod
Accessing logs from a terminated container in a pod when running multiple containers
What is a sidecar and how it could be implemented
What are init containers


PODS

Pods commands

![image](https://github.com/user-attachments/assets/a3d515d3-a0f1-4f46-b9d3-2bc7cbbdc1bd)


comand for the see pod structure in yaml

![image](https://github.com/user-attachments/assets/df2f2771-753d-4f05-bca2-8d2c27de72b9)

Esta seria la salida: 
![image](https://github.com/user-attachments/assets/d03fe625-ae6b-4a38-bfd2-bc4234f86662)

Consultar sobre una politica:

![image](https://github.com/user-attachments/assets/3e8f7cca-4306-479b-91ab-f1b634c248df)

La flag -f 
![image](https://github.com/user-attachments/assets/9e155a0e-c06e-4898-9554-3ba02e7b5112)


Questions

How do you run a command inside a specific container in a running pod?
- kubect exec -it -c --

What is the command to create a port-forward tunnel in Kubernetes for testing purposes?
- kubectl port-forward pod/:

How can you see logs of a particular container from a multi-container pod?
- kubectl logs -c

Which command would you use to view the logs of a container that has crashed and restarted?
- kubectl logs pod/ -c-p

How do you run a pod with a specific image in Kubernetes?
- kubectl run nginx --image=nginx

What is the Kubernetes object YAML configuration management command that provides a declarative approach?
- kubectl apply -f

In Kubernetes, what is the purpose of a sidecar container in a pod?
- To perform a specific task in tandem with the main container

Importante: Kubernetes network model allows pods to communicate without NAT. True or False?
True.
Importatnte El modelo de red de Kubernetes (Kubernetes network model) permite que los pods se comuniquen entre sí sin necesidad de Traducción de Direcciones de Red (NAT). Cada pod en Kubernetes recibe su propia dirección IP, y los pods pueden comunicarse directamente entre sí a través de estas direcciones IP, siempre y cuando estén en la misma red o puedan enrutar los paquetes entre sí. Este modelo de red plana simplifica la configuración de la red y asegura que todos los pods sean accesibles entre sí dentro del clúster.

Which command is used to execute an interactive shell inside a running container in a Kubernetes pod?
- kubectl exec -it -c -- bash

Which Linux namespace is the default shared in a Kubernetes Pod?
- Network Namespace

What is a valid container restart policy in Kubernetes?
Never
OnFailure
Always
correctAll of the above (Correcta!!)

What command allows you to view the YAML declaration specification from the command line?
- kubectl explain [object]
Adicional: Si Ejecutamos el comando con el explain podemos ver lo siguiente: 
![image](https://github.com/user-attachments/assets/36e803bc-7fb3-427f-8ada-2ff3c7151e08)





Namespace de Red en Pods de Kubernetes

Namespace de Red o NETWORK NAMESTPACE : Todos los contenedores dentro de un Pod comparten el mismo namespace de red. Esto significa que todos comparten la misma dirección IP y las interfaces de red. Pueden comunicarse entre sí a través de localhost y también acceder a la red usando la misma dirección IP asignada al Pod. Este namespace de red compartido permite que los contenedores sean conscientes de los demás y se comuniquen directamente entre ellos a través de su red local.

Otros Namespaces en Pods de Kubernetes
Kubernetes también puede manejar otros tipos de namespaces, pero no se comparten entre los contenedores de la misma manera que el namespace de red. Aquí hay un breve resumen de cómo se manejan los diferentes namespaces:

Namespace PID: Por defecto, cada Pod tiene su propio namespace PID, lo que aísla los IDs de proceso de los contenedores dentro del Pod de los de otros Pods. Los contenedores dentro del mismo Pod pueden ver los procesos entre sí y comunicarse usando mecanismos IPC.

Namespace IPC: Cada Pod tiene su propio namespace IPC por defecto, lo que aísla los recursos de comunicación entre procesos como semáforos y memoria compartida. Los contenedores dentro del mismo Pod pueden compartir recursos IPC.

Namespace UTS: Cada Pod tiene su propio namespace UTS (Unix Timesharing System), lo que aísla la información del nombre de host y del dominio. Esto significa que cada Pod puede tener su propio nombre de host, pero los contenedores dentro del mismo Pod comparten el nombre de host.

Namespace de Montaje: Los contenedores dentro de un Pod comparten el mismo namespace de montaje, lo que significa que comparten la misma vista del sistema de archivos y pueden ver los mismos volúmenes montados en el Pod.


Si el pod tiene múltiples contenedores, debes especificar el contenedor del cual quieres ver los logs:
kubectl logs <nombre-del-pod> -c <nombre-del-contenedor>





Sidecar Containers

Sidecar containers are the secondary containers that run along with the main application container within the same Pod. These containers are used to enhance or to extend the functionality of the primary app container by providing additional services, or functionality such as logging, monitoring, security, or data synchronization, without directly altering the primary application code.

Typically, you only have one app container in a Pod. For example, if you have a web application that requires a local webserver, the local webserver is a sidecar and the web application itself is the app container.

Leer: https://network-insight.net/2016/03/19/kubernetes-network-namespace/#:~:text=In%20simple%20terms%2C%20a%20network,in%20its%20virtual%20network%20environment.

<h2>kubectl get SC</h2> 

El comando kubectl get sc se utiliza para obtener información sobre los StorageClasses en un clúster de Kubernetes. Las StorageClasses son recursos de Kubernetes que definen diferentes tipos de almacenamiento que se pueden utilizar para los Persistent Volumes (PV) y Persistent Volume Claims (PVC). Cada StorageClass puede tener diferentes parámetros de configuración, como el tipo de almacenamiento (por ejemplo, SSD o HDD), la política de provisión y otros detalles específicos del proveedor de almacenamiento.

Comando
Para listar las StorageClasses disponibles en tu clúster, usa:


Comando: kubectl get sc


La salida típica del comando kubectl get sc puede verse así:

Copiar código
NAME                 PROVISIONER                RECLAIMPOLICY   VOLUMEBINDINGMODE   ALLOWVOLMODE   AGE
standard (default)   kubernetes.io/aws-ebs      Delete          WaitForFirstConsumer   Filesystem      10d
fast                 kubernetes.io/gce-pd       Retain          Immediate             Block           5d


Explicación de los Campos
NAME: El nombre de la StorageClass.
PROVISIONER: El provisionador que gestiona el almacenamiento. Esto puede variar dependiendo del proveedor de almacenamiento (por ejemplo, kubernetes.io/aws-ebs para AWS EBS).
RECLAIMPOLICY: La política de reclamación que determina qué hacer con los volúmenes cuando se elimina un PVC. Puede ser Delete (el volumen se elimina) o Retain (el volumen se conserva).
VOLUMEBINDINGMODE: El modo de enlace del volumen. Puede ser Immediate (el volumen se enlaza inmediatamente al PVC) o WaitForFirstConsumer (el volumen se enlaza cuando un pod consume el PVC).
ALLOWVOLMODE: El modo de acceso permitido para el volumen. Puede ser Filesystem o Block.
AGE: El tiempo transcurrido desde que se creó la StorageClass.



Print the logs for a container in a pod. 


If the pod has only one container, the container name is optional.

kubectl logs [-f] [-p] POD [-c CONTAINER]
Examples
# Return snapshot logs from pod nginx with only one container
kubectl logs nginx

# Return snapshot of previous terminated ruby container logs from pod web-1
kubectl logs -p -c ruby web-1

# Begin streaming the logs of the ruby container in pod web-1
kubectl logs -f -c ruby web-1

# Display only the most recent 20 lines of output in pod nginx
kubectl logs --tail=20 nginx

# Show all logs from pod nginx written in the last hour
kubectl logs --since=1h nginx
Options
  -c, --container="": Print the logs of this container
  -f, --follow[=false]: Specify if the logs should be streamed.
      --limit-bytes=0: Maximum bytes of logs to return. Defaults to no limit.
  -p, --previous[=false]: If true, print the logs for the previous instance of the container in a pod if it exists.
      --since=0: Only return logs newer than a relative duration like 5s, 2m, or 3h. Defaults to all logs. Only one of since-time / since may be used.
      --since-time="": Only return logs after a specific date (RFC3339). Defaults to all logs. Only one of since-time / since may be used.
      --tail=-1: Lines of recent log file to display. Defaults to -1, showing all log lines.
      --timestamps[=false]: Include timestamps on each line in the log output.



<h2>Kubernetes Namespaces</h2>

<h3>Kubernetes Namespaces - Study Tips</h3>

The upcoming video in our KCNA examination preparation series dives deeply into the topic of namespaces in Kubernetes. This video extends far beyond the basic concepts of creating and utilising a namespace to fully aid you in your preparation for the exam -

Key areas to concentrate on include:

Default Namespaces in Kubernetes: Understand the predefined namespaces that come with a Kubernetes cluster and their specific purposes
Kubernetes API Objects and Namespaces: Kubernetes API objects that can operate within namespaces. Specific focus should be given to ResourceQuotas and LimitRanges
Role-Based Access Control (RBAC) in Relation to Namespaces: The purpose of RBAC and the relationship with namespaces
Namespaced vs Non-Namespaced Kubernetes Components: The distinction between namespaced and non-namespaced components in Kubernetes, such as the difference between pods (namespaced) and nodes (non-namespaced)
Kubernetes resources: How to list resources and how to check if a resource is namespaced or non-namespaced

Namespaces Benefits

![image](https://github.com/user-attachments/assets/3c148f63-3393-488d-8106-d885ad3e930f)


Nameespaces Questions


What is a key benefit of using Kubernetes Namespaces?
- Limitation of Kubernetes functionality
- Increasing the CPU usage of applications
- Combining cluster resources
- Isolating resources and limiting the scope of user privileges (Correct)



How can you describe a namespace within a Kubernetes cluster?
- A storage system for the Kubernetes cluster
- A communication protocol used by the Kubernetes system
- A type of container orchestrator like Kubernetes itself
- A virtual cluster within Kubernetes, used for isolating resources (Correct)

Which command is used to view all resources within all namespaces in a Kubernetes cluster?
- kubectl get all
- kubectl get all -A (Correct)
- kubectl get -A
- kubectl get namespaces


What is the purpose of the 'kube-system' namespace in Kubernetes?
- It is designed for user deployed applications
- It is for objects created by the Kubernetes system (Correct)
- It is a namespace that is readable by all users
- It holds lease objects associated with individual nodes


If you run a command without specifying a namespace in Kubernetes, which namespace will it run in?
- kube-public
- kube-system
- kube-node-lease
- default (Correct)


How can a new namespace be created in Kubernetes?
- kubectl create nsp mynamespace
- kubectl new namespace mynamespace
- kubectl create namespace mynamespace (Correct)
- kubectl add namespace mynamespace

  

How can you run a pod in a specific namespace in Kubernetes?
- kubectl run pod --nsp=mynamespace
- kubectl run pod --n=mynamespace
- correctkubectl -n mynamespace run pod (Correct)
- kubectl --ns=mynamespace run pod


Which namespace is readable by all users, including those who are not authenticated?
- kube-public (Correct)
- kube-system
- mynamespace
- default

How can you delete a pod named 'nginx' in a specific namespace called mynamespace in Kubernetes?
- kubectl delete pod/nginx --grace-period=0
- kubectl -n mynamespace delete pod/nginx (correct)
- kubectl delete pod/nginx --namespace=all
- kubectl -namespace mynamespace delete pod/nginx


What are the default namespaces provided with a standard Kubernetes installation?
- default, kube-system, kube-public, kube-node-lease (Correct)
- kube-system, mynamespace, kube-public, kube-node-lease
- default, mynamespace, kube-public, kube-node-lease
- default, kube-system, kube-public


If a resource is "Namespaced" in Kubernetes, what does this mean?
- It exists independently of namespaces
- correctIt is tied to a particular Namespace and exists within the context of that Namespace (Correct)
- It is a cluster-level resource
- It is not affected by namespaces at all



What command will change the current context to use a specific namespace?
- kubectl config set-context --current --namespace=mynamespace (Correct)
- kubectl config set-context --namespace=mynamespace
- kubectl set-context --current --namespace=mynamespace
- kubectl context set --current --namespace=mynamespace


What will happen to the resources inside a namespace if the namespace is deleted in Kubernetes?
- The resources will be moved to the default namespace
- The resources will also be deleted (Correct)
- The resources will be moved to a new namespace
- The resources will be left without a namespace


<h2>Kubernetes Deployments and ReplicaSets</h2>

- Replication: Should a pod crash or get deleted, the Deployment makes sure the number of pods is as expected.
- Updates: Updates are phased out gradually to prevent all instances from being updated simultaneously.
- Rollbacks: If anything goes wrong during the update or while a new version is running, Deployments allow you to revert to an older version.

![image](https://github.com/user-attachments/assets/778e6aa2-3d29-489b-9f6a-f61602a1fd82)

<h3>Commands Importants</h3>

kubectl rollout history: Manage the rollout of one or many resources.
- Valid resource types include:

- deployments
- daemonsets
- statefulsets
kubectl rollout SUBCOMMAND
Examples
  # Rollback to the previous deployment
  kubectl rollout undo deployment/abc
  
  # Check the rollout status of a daemonset
  kubectl rollout status daemonset/foo
  
  # Restart a deployment
  kubectl rollout restart deployment/abc
  
  # Restart deployments with the 'app=nginx' label
  kubectl rollout restart deployment --selector=app=nginx


Adicional: kubectl rollout es un comando esencial en Kubernetes que nos permite gestionar las actualizaciones de nuestros despliegues de forma controlada y segura. Sirve para:

Iniciar actualizaciones: Cuando modificamos un Deployment (por ejemplo, cambiando la imagen de contenedor, ajustando el número de réplicas o realizando cambios en la configuración), podemos utilizar kubectl rollout para iniciar el proceso de actualización.
Pausar, reanudar y reiniciar actualizaciones: Si durante una actualización detectamos un problema, podemos pausarla con kubectl rollout pause para investigar y solucionar el inconveniente. Una vez resuelto, podemos reanudarla con kubectl rollout resume o incluso reiniciarla desde el principio con kubectl rollout restart.
Ver el historial de actualizaciones: Con kubectl rollout history podemos ver todas las revisiones anteriores de un Deployment, lo que nos permite revertir a una versión anterior si es necesario.
Revertir actualizaciones: Si una actualización causa problemas, podemos utilizar kubectl rollout undo para revertir a una revisión anterior estable.
Obtener el estado de una actualización: Con kubectl rollout status podemos monitorear el progreso de una actualización y verificar si se ha completado correctamente.


¿Por qué es útil kubectl rollout?

Actualizaciones progresivas: Permite realizar actualizaciones de forma gradual, reduciendo el riesgo de interrupciones en el servicio.
Control y visibilidad: Nos brinda herramientas para controlar el proceso de actualización y monitorear su estado.
Reversibilidad: Permite revertir fácilmente a una versión anterior en caso de problemas.
Automatización: Se puede integrar en pipelines de CI/CD para automatizar el proceso de despliegue.
Ejemplo de uso:

Supongamos que tenemos un Deployment llamado my-app y queremos actualizarlo a una nueva versión de la imagen de contenedor. Podemos ejecutar el siguiente comando:

Bash
kubectl rollout restart deployment/my-app
Usa el código con precaución.

Este comando reiniciará el proceso de actualización, aplicando los nuevos cambios al Deployment.

En resumen, kubectl rollout es una herramienta fundamental para gestionar las actualizaciones de nuestros despliegues en Kubernetes de manera segura y eficiente. Nos proporciona un alto grado de control y flexibilidad para realizar cambios en nuestras aplicaciones sin afectar la disponibilidad del servicio.

¿Tienes alguna otra pregunta sobre kubectl rollout o Kubernetes en general? Estaré encantado de ayudarte.

Temas relacionados que podrías encontrar interesantes:

Deployment en Kubernetes: ¿Qué es un Deployment y cómo funciona?
ReplicaSet en Kubernetes: ¿Cuál es la relación entre Deployment y ReplicaSet?
Estrategias de actualización en Kubernetes: ¿Cuáles son las diferentes estrategias de actualización disponibles?



kubectl annotate es otro comando esencial en Kubernetes que nos permite agregar metadatos adicionales a cualquier recurso del clúster. Estos metadatos, llamados anotaciones, son pares clave-valor que se almacenan junto con el recurso y se pueden utilizar para diversas finalidades.

¿Para qué sirve kubectl annotate?

Marcar recursos: Podemos utilizar anotaciones para marcar recursos con información relevante, como etiquetas de entorno, información de propiedad, o cualquier otro dato que queramos asociar a un recurso.
Controlar políticas: Algunas herramientas o políticas pueden basarse en las anotaciones de los recursos para tomar decisiones. Por ejemplo, un controlador de políticas podría permitir o bloquear ciertas operaciones basadas en el valor de una anotación específica.
Integración con herramientas externas: Las anotaciones se pueden utilizar para integrar Kubernetes con herramientas externas. Por ejemplo, una herramienta de monitoreo podría usar anotaciones para identificar recursos específicos o una herramienta de backup podría utilizarlas para filtrar los recursos que se deben incluir en las copias de seguridad.
Personalización: Las anotaciones nos permiten personalizar los recursos según nuestras necesidades y requisitos.
Ejemplo de uso:

Supongamos que tenemos un Deployment llamado my-app y queremos agregar una anotación para indicar que pertenece al entorno de producción:

Bash
kubectl annotate deployment/my-app environment=production
Usa el código con precaución.

Esto agregará la anotación environment=production al Deployment my-app.

Para ver las anotaciones de un recurso:

Bash
kubectl describe deployment/my-app


En resumen, kubectl annotate es una herramienta versátil que nos permite agregar metadatos personalizados a los recursos de Kubernetes. 
Estos metadatos pueden ser útiles para una variedad de propósitos, desde la organización y clasificación de recursos hasta la integración con herramientas externas.


<h4>Properties in deployments</h4>

MaxSurge (Porcent): This allows Kubernetes to increase the number of Pods by  % (porcent) above the desired amount during an update, maintaining application availability.

MaxUnavailable (Porcent): Up to (Porcent) % of the Pods can be unavailable during the update process, ensuring availability whilst limiting resource usage.

![image](https://github.com/user-attachments/assets/d3dc88b7-06d3-43a2-9072-49e0dbd71eee)

<h2>Questions</h2>

What is the function of Kubernetes Deployment?
- It offers a non-declarative way to manage applications
- It decreases the number of Pod Replicas
- It provides an object that delivers declarative updates for applications (correct)
- It serves to manually manage Pods

What feature of Deployments ensures the number of Pods is as expected in case of a Pod crash or deletion?
- Updates
- Rollbacks
- Replication (correct)
- Deployment Strategies

Which Kubernetes feature allows you to revert to an older version of an application during a problematic update?
- Replication
- Updates
- Rollbacks (correct)
- Deployment Strategies

When scaling the number of Deployment replicas, which command is used?
- kubectl get
- kubectl annotate
- kubectl rollout
- kubectl scale (correct)
  

What does the maxSurge: 25% setting in the deployment strategy signify?
- It allows Kubernetes to reduce the number of Pods by 25% below the desired amount during an update
- It allows Kubernetes to increase the number of Pods by 25% above the desired amount during an update
- It makes up to 25% of the Pods unavailable during the update process (correct)
- It makes up to 25% of the Pods surge beyond their capacity during an update


What does the maxUnavailable: 25% setting in a Kubernetes Deployment strategy signify?
- Up to 25% of the Pods can be unavailable during the update process (correct)
- Up to 25% of the Pods can surge beyond their capacity during an update
- It allows Kubernetes to increase the number of Pods by 25% above the desired amount during an update
- It allows Kubernetes to reduce the number of Pods by 25% below the desired amount during an update

What is the effect of changing the image of a Deployment?
- It creates a new Deployment
- It removes the current ReplicaSet
- It creates a new ReplicaSet (correct)
- It has no significant effect


How can you monitor a Kubernetes Deployment's update in real time?
- Using the command 'kubectl rollout status deployment/' (correct)
- Using the command 'kubectl describe deployment'
- Using the command 'kubectl get replicaset -o wide'
- Using the command 'kubectl get pods'


In case of a Deployment failure, which Kubernetes command can be used to revert to a functioning version?
- kubectl get pods
- kubectl set image
- kubectl rollout undo deployment/ (correct)
- kubectl describe deployment

What happens when you roll back to a specific revision of a Deployment?
- It erases the entire rollout history
- It creates a new ReplicaSet
- It reuses the original ReplicaSet and becomes the latest revision (correct)
- It results in a Deployment failure

What is the purpose of 'kubectl annotate' command in Kubernetes?
- To modify the configuration of an existing object
- To add annotations to an object (correct)
- To create a new object
- To delete an existing object

What happens when you delete a Kubernetes Deployment?
- The Deployment is deleted, but the linked ReplicaSets remain
- The linked ReplicaSets are deleted, but the Deployment remains
- Both the Deployment and the linked ReplicaSets are deleted (correct)
- Neither the Deployment nor the linked ReplicaSets are deleted

What is the recommended object for running applications in a Kubernetes cluster?
- Nodes
- Pods
- Services
- Deployments (correct)



<h2>Minikube Commands</h2>

<ul>
    <li><code>minikube start --profile [profile-name]</code>: create new cluster and start.</li>
    <li><code>minikube delete --profile [profile-name]</code>: delete minikube profile.</li>
    <li><code>minikube profile [profile-name]</code>: choose profile in minikube.</li>
    <li><code>minikube-help</code>: see all commands and how works with minikube.</li>
    <li><code>minikube profile list</code>: see list of profiles in minikube.</li>
    <li>minikube start -p [profile-name]</li>
    <li>minikube status</li>
    <li>minikube logs</li>
    <li>minikube service [service-name]  —url: nos permite hacer un tunning de un servicio que queramos en macOS. Para exponerlo publicamente. </li>
    <li>minikube start --driver=docker -p cluster-development --nodes=2 (Crea un cluster a partir de la cantidad de nodos que le indiquemos)</li>
</ul>
Para ver mas comandos de minikube: https://minikube.sigs.k8s.io/docs/commands/



<h2>Services</h2>

Servicios:

Un servicio es un componente de Kubernetes que tiene como proposito principal exponer un recurso fuera del cluster.

![image](https://github.com/user-attachments/assets/eea19e39-cdda-4def-b3d8-e35813c54c3b)

Que es un servicio?

Son los componentes que nos van a permitir conectarnos con el mundo exterior. Es un componente intermedio que lo unico que hace   es actuar entre el cliente y nuestro deployment.El servicio detecta cuando un pod se cae, estados, si se esta levantando etc. Lo hace mediante Selectors. y apartir de los labels que tengan los pods.

Los tipos de servicios se describen mas abajo, dejamos una imagen representativa (Pendiente)

![image](https://github.com/user-attachments/assets/410b323c-4c56-4bfc-9740-ad1eef4b6ba0)



Crear un Servicio de tipo NodePort:

kubectl expose deploy [deploy-name] —port=[port-number] —type=[type-port]: le decimos que nos cree un servicio de tipo nodeport especificando el puerto y el nombre del deploy. Ejemplo: kubectl expose deploy apache --port=80 --type=NodePort 




Cluster IP
![image](https://github.com/user-attachments/assets/20e4b8a4-b50e-4f19-87cc-cdadf490ba5f)



* Importante (a tener en cuenta):

Esto lo podremos visualizar que se usa junto a algunos comandos <strong>—dry-run=client</strong>: Esta opción permite simular la creación del deployment sin que se aplique realmente al clúster. Es útil para verificar que el comando funciona correctamente antes de ejecutarlo de forma real.


<h3>Commands</h3>

kubectl get svc: get services
kubectl expose [service-name]: expose service
kubectl expose deployment/nginx -type=[type-service] —port 8080 -target-port 80: expose service by types and after add the port entry and port listener.



<h3>Questions</h3>

Which Kubernetes component provides a way to expose an application running on a set of Pods as a network service?
- ConfigMap
- Namespace
- Deployment
- Service (correct)


Which of the following is NOT one of the primary service types available in Kubernetes to expose services?
- ClusterIP
- NodePort
- LoadBalancer
- SwitchBalancer (correct)

What is the default service in Kubernetes that establishes a service with an internal IP address, reachable only within the cluster?
- NodePort
- LoadBalancer
- ClusterIP (correct)
- ExternalName


Which Kubernetes service type allows services to be technically available outside of the cluster, if your nodes IP address are externally accessible?
- Headless
- ClusterIP 
- NodePort (correct)
- ExternalName

What is the service type in Kubernetes that creates what would be in DNS terms, a CNAME, i.e. an alias of another domain?
- LoadBalancer
- ExternalName (correct)
- NodePort
- ClusterIP

What is a "Headless" service in Kubernetes?
- A service that does not use any of the 4 main types of services
- A ClusterIP service that has no IP (correct)
- A service that cannot be accessed via DNS
- A NodePort service that does not have any nodes assigned


<strong>Por que de esto? Explicacion</strong>

Un servicio "Headless" en Kubernetes se define como un servicio ClusterIP que no tiene IP.
Cuando creas un servicio headless, configuras el campo clusterIP en None. Esto permite que el servicio omita el mecanismo de balanceo de carga estándar y devuelva directamente los puntos finales (pods) individuales cuando se consulta. Esto es útil para aplicaciones que necesitan descubrir las IPs de los pods directamente, como los StatefulSets.




Which Kubernetes service type is dependent on your Kubernetes offering and may vary significantly between On-Prem and Cloud?
- NodePort
- LoadBalancer (correct)
- ClusterIP 
- ExternalName

<strong>Por que de esto? Explicacion</strong>
El tipo de servicio de Kubernetes que es particularmente dependiente de la oferta de Kubernetes y puede variar significativamente entre entornos on-premises y en la nube es LoadBalancer.

En entornos en la nube, el tipo de servicio LoadBalancer suele provisionar un balanceador de carga de la nube que expone el servicio externamente. Sin embargo, en entornos on-premises, puede que no tengas un servicio de balanceo de carga integrado, lo que significa que tendrías que configurar un balanceador de carga externo manualmente o usar otro enfoque.
En cambio, los tipos de servicio NodePort, ClusterIP y ExternalName son más consistentes en su comportamiento a través de diferentes entornos.




Which Kubernetes service is only accessible within the cluster?
- NodePort
- ClusterIP (correct)
- LoadBalancer
- ExternalName


What do EndPoints in Kubernetes represent?
- The IP addresses assigned to the nodes that the service points to
- The IP addresses assigned to the pods that the service points to (correct)
- The storage volumes assigned to the pods
- The routes assigned to the services in the Kubernetes cluster


What does the command 'kubectl expose' do in Kubernetes?
- It exposes a Kubernetes node to the external network
- It exposes a Kubernetes deployment as a service (correct)
- It exposes the Docker runtime on a Kubernetes node
- It exposes a Kubernetes pod to other pods in the same namespace


What is the primary use case of a ClusterIP service in Kubernetes?
- To expose applications to the external world
- To establish a service with an internal IP address, reachable only within the cluster (correct)
- To load balance requests to multiple pods
- To create an alias for another domain


What is the function of a LoadBalancer service type in Kubernetes?
- To create an internal service reachable only within the cluster
- To provide a mechanism for automatic load distribution across multiple nodes and pods (correct)
- To provide a mechanism to access services using friendly names
- To create a DNS alias for another domain


What is the distinguishing feature of a Headless service in Kubernetes?
- It exposes a service with an internal IP address
- It provides a DNS implementation with no proxy, so each pod handles its own traffic (correct)
- It provides an alias for another domain
- It assigns a specific port on each node to the service

<strong>Por que de esto? Explicacion</strong>

La característica distintiva de un servicio headless en Kubernetes es que proporciona una implementación de DNS sin proxy, de modo que cada pod maneja su propio tráfico.Esto significa que cuando consultas el servicio headless, obtienes las direcciones IP individuales de los pods directamente, en lugar de pasar por un balanceador de carga o proxy. Esto permite la comunicación directa con cada pod, lo cual es especialmente útil en escenarios como aplicaciones con estado.



How would you specifically define a Headless Service in a Kubernetes YAML specification?
- By setting spec.clusterIP: None in the Service YAML specification (correct)
- By setting spec.headless: True in the Service YAML specification
- By setting spec.type: Headless in the Service YAML specification
- By setting spec.selector: None in the Service YAML specification


In terms of core abstractions provided by Kubernetes for service networking, how many types of services are primarily defined?
- Three
- Four (correct)
- Five
- Six

<strong>Por que de esto? Explicacion</strong>
Quizas es un poco confusa la respuesta a la pregunta de arriba pero existen 4 tipos de servicios, pero Es la correcta porque dice "In terms of core abstractions provided by Kubernetes for service networking", y hay 4 tipos que hacen parte del core los cuales son: ClusterIP, NodePort, Loadbalancer y ExternalName, el headless no hace parte pero se le considera un tipo que no pertenece al core abstactions.
En Kubernetes, hay varios tipos de servicios que se pueden utilizar para exponer aplicaciones. Los principales tipos son:

> ClusterIP: Este es el tipo de servicio por defecto. Proporciona una dirección IP interna accesible solo dentro del clúster. Es útil para la comunicación entre pods.

> NodePort: Expone el servicio en un puerto específico de cada nodo del clúster. Esto permite acceder al servicio desde fuera del clúster a través de la dirección IP del nodo y el puerto asignado.

> LoadBalancer: Este tipo de servicio se utiliza en entornos de nube. Crea un balanceador de carga externo que distribuye el tráfico entre los pods. Proporciona una dirección IP pública para acceder al servicio desde fuera del clúster.

> ExternalName: Permite crear un servicio que apunta a un nombre de dominio externo. No asigna una IP, sino que actúa como un alias para un nombre DNS externo.

> Headless: Aunque no es un tipo de servicio en el sentido tradicional, se refiere a un servicio ClusterIP configurado con clusterIP: None, lo que permite la resolución de nombres DNS a las IPs de los pods directamente, sin balanceo de carga.


![image](https://github.com/user-attachments/assets/a2b5f368-c073-441f-a6da-879f74836fd2)




<h4>Sobre el Headlees Service del libro Kubernetes in Action</h4>

Well, I think you need some theory. There are many explanations (including the official docs) across the whole internet, but I think Marco Luksa did it the best:

Each connection to the service is forwarded to one randomly selected backing pod. But what if the client needs to connect to all of those pods? What if the backing pods themselves need to each connect to all the other backing pods. Connecting through the service clearly isn’t the way to do this. What is?

For a client to connect to all pods, it needs to figure out the IP of each individual pod. One option is to have the client call the Kubernetes API server and get the list of pods and their IP addresses through an API call, but because you should always strive to keep your apps Kubernetes-agnostic, using the API server isn’t ideal

Luckily, Kubernetes allows clients to discover pod IPs through DNS lookups. Usually, when you perform a DNS lookup for a service, the DNS server returns a single IP — the service’s cluster IP. But if you tell Kubernetes you don’t need a cluster IP for your service (you do this by setting the clusterIP field to None in the service specification ), the DNS server will return the pod IPs instead of the single service IP. Instead of returning a single DNS A record, the DNS server will return multiple A records for the service, each pointing to the IP of an individual pod backing the service at that moment. Clients can therefore do a simple DNS A record lookup and get the IPs of all the pods that are part of the service. The client can then use that information to connect to one, many, or all of them.

Setting the clusterIP field in a service spec to None makes the service headless, as Kubernetes won’t assign it a cluster IP through which clients could connect to the pods backing it.

"Kubernetes in Action" by Marco Luksa


Importante leer articulo: https://cloud.google.com/kubernetes-engine/docs/concepts/service?hl=es-419


<h2>Jobs</h2>

Kubernetes Jobs - Study Tips
For the KCNA examination it is important to have an understanding of both Jobs and CronJobs, please pay particular attention to the following in the next video -

A Job vs a CronJob
Completions and Parallelism


Jobs

Jobs represent one-off tasks that run to completion and then stop.
A Job creates one or more Pods and will continue to retry execution of the Pods until a specified number of them successfully terminate. As pods successfully complete, the Job tracks the successful completions. When a specified number of successful completions is reached, the task (ie, Job) is complete. Deleting a Job will clean up the Pods it created. Suspending a Job will delete its active Pods until the Job is resumed again.

A simple case is to create one Job object in order to reliably run one Pod to completion. The Job object will start a new Pod if the first Pod fails or is deleted (for example due to a node hardware failure or a node reboot).

You can also use a Job to run multiple Pods in parallel.

![image](https://github.com/user-attachments/assets/2ccb3080-b16f-4165-b838-5b37121c1204)

Obtener un Job: kubectl get jobs
Crear un job: kubectl run mi-job --image=alpine --restart=Never --command -- echo "Hola Kubernetes"



CronJob

A CronJob starts one-time Jobs on a repeating schedule.
A CronJob creates Jobs on a repeating schedule.

CronJob is meant for performing regular scheduled actions such as backups, report generation, and so on. One CronJob object is like one line of a crontab (cron table) file on a Unix system. It runs a Job periodically on a given schedule, written in Cron format.

CronJobs have limitations and idiosyncrasies. For example, in certain circumstances, a single CronJob can create multiple concurrent Jobs. See the limitations below.

When the control plane creates new Jobs and (indirectly) Pods for a CronJob, the .metadata.name of the CronJob is part of the basis for naming those Pods. The name of a CronJob must be a valid DNS subdomain value, but this can produce unexpected results for the Pod hostnames. For best compatibility, the name should follow the more restrictive rules for a DNS label. Even when the name is a DNS subdomain, the name must be no longer than 52 characters. This is because the CronJob controller will automatically append 11 characters to the name you provide and there is a constraint that the length of a Job name is no more than 63 characters.

- Obtener los Cronjobs: kubectl get cronjobs
- Crear un Cronjob kubectl create cronjob mi-cronjob --image=alpine --schedule="0 3 * * *" -- echo "Hola, Kubernetes CronJob"

![image](https://github.com/user-attachments/assets/4e345e64-d7e5-4224-93f7-58170ed96385)

¿Qué son Job y CronJob en Kubernetes?
Las herramientas de Job y CronJob en Kubernetes se refieren a opciones que contribuyen a realizar labores de manera automatizada y programada, sin que sea necesaria la intervención del usuario.

Job en Kubernetes se utiliza con el objetivo de desarrollar recursos de pods de tipo transitorio, que se encargan de tareas determinadas a las que se encuentran asignados.

Por otro lado, la opción de CronJob en Kubernetes también contribuye a esas acciones, pero tiene la tarea adicional de llevar a cabo la ejecución de labores de acuerdo con un cronograma establecido por el cliente.

Questions:

What is the primary function of a Job in Kubernetes?
- To create a single pod and ensure it runs continuously
- To create one or more pods and ensure a specified number of them successfully terminate (correcta)
- To create multiple nodes and ensure they work together in a cluster
- To manage the scaling of pods within a node


Which command is used to create a Kubernetes job named "calculatepi"?
- kubectl start job calculatepi
- kubectl run job calculatepi
- kubectl initiate job calculatepi
- kubectl create job calculatepi (correcta)

In a Kubernetes Job, what does the parameter completions: 20 signify?
- It specifies the maximum number of retries if the job fails
- It indicates that the job will create 20 pods overall to do the task (correcta)
- It denotes the total number of pods running at any given point in time
- It refers to the total number of nodes on which the job will run


What does the parameter parallelism: 5 signify in a Kubernetes Job specification?
- It represents the number of attempts a failed job will be retried
- It defines the maximum number of pods that should be running in parallel (correcta)
- It signifies the total number of nodes where the job will be parallelized
- It specifies the number of pods to be created for a job


What does the kubectl explain job.spec command do?
- It modifies the existing job specification
- It provides detailed documentation for the structure and fields of a job specification (correcta)
- It creates a new job using the given specification
- It starts the execution of the specified job

What are CronJobs in Kubernetes?
- They are time-based job schedulers (correcta)
- They are random job schedulers
- They are priority-based job schedulers
- They are on-demand job schedulers

What does a CronJob create according to the schedule?
- Pods
- Services
- Deployments 
- Job objects (correcta)


How many completed and failed jobs are kept by default according to the successfulJobsHistoryLimit field in a CronJob?
- 1
- 3 (correcta)
- 5
- 10

Explicacion (Eso aplica para los cronjobs): En Kubernetes, cuando trabajas con un CronJob, el campo successfulJobsHistoryLimit se utiliza para determinar cuántos Jobs exitosos se deben mantener después de que se completen.

De manera predeterminada, el valor de este campo es 3. Esto significa que Kubernetes mantendrá los 3 últimos Jobs exitosos, y eliminará los anteriores. Lo mismo aplica para los Jobs fallidos, pero usando el campo failedJobsHistoryLimit, cuyo valor predeterminado es también 3.



When a CronJob is deleted, what happens to the associated jobs and pods?
- They continue to run
- Only the jobs are deleted, pods continue to run
- Only the pods are deleted, jobs continue to run
- They are deleted along with the CronJob (correcta)





Kubernetes ConfigMaps - Study Tips
For the KCNA examination as well as having an understanding of the use of ConfigMaps, it’s also important to know how to make use of immutable ConfigMaps, a topic we cover in the next video.


<h2>Configmaps</h2>

![image](https://github.com/user-attachments/assets/9b9b8c68-d776-4cbc-b231-9ee3d0579d96)

CONFIGMAPS

Son ficheros que nos van a permitir incorporar un conjunto de propiedades-valor, de una forma muy sencilla, que podamos usarlo automaticamente.

Crear un config map desde la bash:  kubectl create configmap [configmap-name] --from-file=datos_mysql.properties

Info del website oficial

ConfigMaps
A ConfigMap is an API object used to store non-confidential data in key-value pairs. Pods can consume ConfigMaps as environment variables, command-line arguments, or as configuration files in a volume.

A ConfigMap allows you to decouple environment-specific configuration from your container images, so that your applications are easily portable.

Caution:

ConfigMap does not provide secrecy or encryption. If the data you want to store are confidential, use a Secret rather than a ConfigMap, or use additional (third party) tools to keep your data private.
Motivation

Use a ConfigMap for setting configuration data separately from application code.

For example, imagine that you are developing an application that you can run on your own computer (for development) and in the cloud (to handle real traffic). You write the code to look in an environment variable named DATABASE_HOST. Locally, you set that variable to localhost. In the cloud, you set it to refer to a Kubernetes Service that exposes the database component to your cluster. This lets you fetch a container image running in the cloud and debug the exact same code locally if needed.

Note:
A ConfigMap is not designed to hold large chunks of data. The data stored in a ConfigMap cannot exceed 1 MiB. If you need to store settings that are larger than this limit, you may want to consider mounting a volume or use a separate database or file service.
ConfigMap object

A ConfigMap is an API object that lets you store configuration for other objects to use. Unlike most Kubernetes objects that have a spec, a ConfigMap has data and binaryData fields. These fields accept key-value pairs as their values. Both the data field and the binaryData are optional. The data field is designed to contain UTF-8 strings while the binaryData field is designed to contain binary data as base64-encoded strings.

The name of a ConfigMap must be a valid DNS subdomain name.

Each key under the data or the binaryData field must consist of alphanumeric characters, -, _ or .. The keys stored in data must not overlap with the keys in the binaryData field.

Starting from v1.19, you can add an immutable field to a ConfigMap definition to create an immutable ConfigMap.

ConfigMaps and Pods

You can write a Pod spec that refers to a ConfigMap and configures the container(s) in that Pod based on the data in the ConfigMap. The Pod and the ConfigMap must be in the same namespace.

Note:
The spec of a static Pod cannot refer to a ConfigMap or any other API objects.
Here's an example ConfigMap that has some keys with single values, and other keys where the value looks like a fragment of a configuration format.

Example:

apiVersion: v1
kind: ConfigMap
metadata:
  name: game-demo
data:
  # property-like keys; each key maps to a simple value
  player_initial_lives: "3"
  ui_properties_file_name: "user-interface.properties"

  # file-like keys
  game.properties: |
    enemy.types=aliens,monsters
    player.maximum-lives=5    
  user-interface.properties: |
    color.good=purple
    color.bad=yellow
    allow.textmode=true    

   
Crear confirmar directamente desde la bash
kubectl create configmap [configmap-name] --from-literal=usuario=usu1 --from-literal=password=pass1
  

<h2>Questions</h2>


Which of the following commands can be used to create a Kubernetes ConfigMap with specific values using the command line interface?
- kubectl make configmap colour-configmap --from-literal=COLOUR=red --from-literal=KEY=value
- kubectl put configmap colour-configmap --from-literal=COLOUR=red --from-literal=KEY=value
- kubectl add configmap colour-configmap --from-literal=COLOUR=red --from-literal=KEY=value
- kubectl create configmap colour-configmap --from-literal=COLOUR=red --from-literal=KEY=value (correcta)


How can you check a Kubernetes ConfigMap’s values?
- kubectl explain configmap/colour-configmap
- kubectl review configmap/colour-configmap
- kubectl describe configmap/colour-configmap (correcta)
- kubectl read configmap/colour-configmap


Which of the following commands is used to create a ConfigMap in Kubernetes from a file containing key-value entries?
- kubectl create configmap colour-configmap --from-env-file=configmap-colour.properties (correcta)
- kubectl create configmap colour-configmap --from-file=configmap-colour.properties
- kubectl add configmap colour-configmap --from-env-file=configmap-colour.properties
- kubectl update configmap colour-configmap --from-env-file=configmap-colour.properties



How can a pod be configured to use a ConfigMap's values?
- By using the 'envFrom' field in the pod's yaml specification (correcta)
- By manually entering the ConfigMap's values into the pod's environment variables
- By linking the pod to the ConfigMap's location
- By copying the ConfigMap's file into the pod's file system



How can a pod be configured to use a ConfigMap's values?
- By using the 'envFrom' field in the pod's yaml specification (correcta)
- By manually entering the ConfigMap's values into the pod's environment variables
- By linking the pod to the ConfigMap's location
- By copying the ConfigMap's file into the pod's file system


What happens when you set a Kubernetes ConfigMap as 'immutable'?
- It can't be deleted
- It can't be changed once set (correcta)
- It can't be used by pods
- It can't be listed by kubectl


What is a significant advantage of using ConfigMaps in Kubernetes?
- They provide a centralised location for configuration data on the cluster (correcta)
- They increase the speed of pod creation
- They secure the cluster from external threats
- They automate the deployment process



What Kubernetes version provided a feature as stable that allows a ConfigMap to be immutable?
- Kubernetes 1.19
- Kubernetes 1.20
- Kubernetes 1.21 (correcta)
- Kubernetes 1.22


Secrets

![image](https://github.com/user-attachments/assets/57e1f494-dffe-4c36-a19d-35d685f2e5f7)



*** SECRETS ***

•Un secret es un recurso dentro de Kubernetes permite guardar información confidencial dentro de kubernetes, Por ejemplo contraseñas tokens de autorización, claves SSH, etcétera. Los Secrets estan codificados en base64. Debemos saber cual es la diferencia entre encriptacion y codificación. Los secrets no sirven para encriptar, solo codifican en base64.


Normalmente nos sirven como método de autentificación para acceder a distintos recursos protegidos dentro de kubernetes, desde los componentes internos hasta nuestras propias aplicaciones. 
Disponemos de distintos tipos de Secrets orientados a distintos recursos dentro de la infraestructura.
La forma más directa de utilizar estos Secrets dentro de kubernetes es asociándolos a un POD. 


Tipos de Secrets (*** Importante ***)

Opaque: Tipo por defecto que contiene cualquier información que queramos incluir y proteger. 
  • Service account token: Almacena un token que identifica un Service Account. Veremos posteriormente este recurso cuando hablemos del tema de seguridad Pero básicamente representan una identidad para los procesos que se ejecutan dentro de un POD.
  • Docker config: Almacena las credenciales necesarias para poder acceder a un registro privado de Docker. 
  • Basic authentication: Credenciales que se utilizan para la autenticación básica contiene realmente dos propiedades obligatorias: username y password.

SSH: Almacenan las credenciales para poder autenticarnos a través de SSH. vamos a necesitar una propiedad denominada 'ssh-privatekey' que en realidad es un par de clave valor.

TLS: almacenan un certificado y su clave asociada que se utilizan habitualmente para TLS. su caso más habitual es usarlo con un recurso de tipo ingres, es decir para acceder desde el exterior del clúster. en este caso deberemos de tener estos dos valores: 'tls.key' y ‘tls.crt’.

Bootstrap: Estos tokens son bastante especiales y se utiliza para el proceso bootstrap del nodo.



Comando para obtener los secrets

kubectl get secrets

Comando para crear un Secret:

kubectl create secret generic [secret-name] --from-literal=[key]=[value] --from-literal=[key]=[value]


Comando para crear un Secret a partir de un archivo:

kubectl create secret generic datos --from-file=datos.txt

Comando de Linux que nos permite decodificar lo que tenemos codificado entre comillas del comando:

echo "dXN1MQ==" | base64 --decode; echo;






Diferencia entre un Secret y un Configmap

![image](https://github.com/user-attachments/assets/1ec7d01c-ca3b-48ab-9ae0-6fe261046f2e)



<h2>Questions</h2>


What is the purpose of using Kubernetes Secrets?
- To store and manage sensitive information like passwords, tokens, keys, etc. (correct)
- To store and manage public configuration data
- To store and manage an application's code
- To store and manage the application's log data


What is the difference between a Secret and a ConfigMap in Kubernetes?
- ConfigMaps store sensitive data while Secrets store non-sensitive data
- Secrets are for storing confidential information while ConfigMaps are for non-secret configuration data (correct)
- Secrets and ConfigMaps serve the same purpose and have no differences
- Secrets are used for storing an application's code while ConfigMaps are used for storing sensitive data


How is the sensitive data stored in Kubernetes Secrets?
- It is encrypted
- It is hashed
- It is encoded (correct)
- It is stored in plain text


What is the encoding mechanism used in Kubernetes Secrets?
- MD5
- SHA-256
- RSA
- Base64 (correct)



What is the potential risk when using secrets in Kubernetes?
- If someone gains access to etcd or retrieves the secret as yaml, they could potentially get the value 
- The secrets can be easily hacked (correct)
- The secrets can be lost if the cluster crashes
- The secrets cannot be backed up


What command is used to create a secret in Kubernetes?
- kubectl create secret (correct)
- kubectl apply secret
- kubectl update secret
- kubectl secret create


What type is assigned when creating a generic secret in Kubernetes?
- TypeGeneric
- Generic
- TypeSecret
- Opaque (correct)




<h2>Kubernetes Labels - Study Tips</h2>
For the KCNA examination, general knowledge of labels and scenarios in which they could be utilised is required.

![image](https://github.com/user-attachments/assets/e8f177f0-d27b-4d8b-96ea-ef8f9a97af64)


Label Selectors and Annotations

Labels: las labels son etiquetas que les ponemos a los objetos. Identifican a nuestros componentes y Nos permite mejorar la metadata.

Ejemplos:

kubectl get pod [pod-name] --show-labels: Nos permite ver las etiquetas de un determinado objeto, en este caso de un determinado pod.

kubectl label pod [pod-name] [tag-name]=[value-tag] : Añadir una etiqueta

kubectl label --overwrite pod [pod-name] [tag-name]= [new-value-tag]: Actualizar una etiqueta.

kubectl label pod [pod-name] [tag-name]- : tal cual y con el guion, nos permite eliminar una etiqueta de nuestro pod.


Selectores: son como condiciones, condiciones que yo utilizo para localizar objetos que tengan determinadas etiquetas. Es decir, pongo etiquetas a las labels y posteriormente mediante los selectores intento localizar ese tipo de objetos.
-l : para buescar un determinado label, ejemplo: kubectl get pods --show-labels -l [tag-name]=[tag-value]
Selector con condicion (las condiciones siempre son del tipo AND): kubectl get pods --show-labels -l [conditions]
ejemplo: kubectl get pods --show-labels -l ambiente=desarrollo,responsable=jose-osorio, otro ejemplo: kubectl get pods --show-labels -l ambiente!=desarrollo.

* Condiciones mediante conjuntos: kubectl get pods —show-labels -l ‘ambiente in(desarrollo)’, otro ejemplo: kubectl get pods —show-labels -l ‘ambiente in(desarrollo, testing)’; kubectl get pods —show-labels -l ‘ambiente in(desarrollo)’, otro ejemplo: kubectl get pods —show-labels -l ‘ambiente notin(desarrollo, testing)’

Lo mejor es que se puede con todos los comandos, por ejemplo para el delete: kubectl delete pods -l ambiente=desarrollo


Anotaciones: son descriptivas, tambien se basan en el standar clave valor. Sirven para describir y documentar nuestros componentes.

Ejemplo: kubectl get pod [pod-name] -o [format]=[busqueda por] - kubectl get pod nginx -o jsonpath={.metadata.annotations}, nos va a entregar algo como esto: {
   "adjunto":"ejemplo de anotacion",
   "doc":"se debe cumplir con el empaquetado en jar",
   "kubectl.kubernetes.io/last-applied-configuration":"{\"apiVersion\":\"v1\",\"kind\":\"Pod\",\"metadata\":{\"annotations\":{\"adjunto\":\"ejemplo de anotacion\",\"doc\":\"se debe cumplir con el empaquetado en jar\"},\"labels\":{\"tag-nickname\":\"jcosorio-environment\",\"version\":\"v1\",\"zone\":\"prod\"},\"name\":\"nginx\",\"namespace\":\"default\"},\"spec\":{\"containers\":[{\"image\":\"apasoft/nginx:v1\",\"name\":\"nginx\"}]}}\n"
}

![image](https://github.com/user-attachments/assets/eb2ddf02-e862-45ee-b0de-134af6bb1865)


Questions

How does Kubernetes use labels for resource selection?
- Kubernetes labels have no role in resource selection
- Kubernetes uses labels to select resources for deletion
- Many Kubernetes components use labels to select the resources they should operate on (correct)
- Kubernetes uses labels to select the resources for updating Kubernetes itself


In Kubernetes, how does a service identify which pods it should route traffic to?
- Services use the pod's name to identify them
- Services use the pod's IP address to route traffic
- Services use labels to select the pods they should route traffic to (correct)
- Services use the pod's unique UID to route traffic

What does the "--selector" option do in a "kubectl get" command?
- It selectively renames the resources based on the provided label
- It selectively deletes resources based on the provided label
- It filters and displays resources based on the provided label (correct)
- It selectively changes the status of resources based on the provided label
  

What is the difference between the "-l" and "--selector" options in Kubernetes commands?
- "-l" is used to filter resources based on labels, while "--selector" is used to specify selectors in the command
- "-l" and "--selector" have completely different functionalities in Kubernetes commands
- "-l" and "--selector" both are used to filter resources based on labels and are interchangeable (correct)
- "-l" is used to set labels, while "--selector" is used to filter resources based on labels


How can labels be used to create 'scopes' or 'environments' within a Kubernetes cluster?
- Labels cannot be used to create 'scopes' or 'environments'
- Labels can be used to designate resources as belonging to groups such as 'development', 'testing', or 'production' (correct)
- Labels can be used to isolate resources in different namespaces
- Labels can be used to enforce resource limits on different environments


What operational benefits can be derived from the effective use of labels in a Kubernetes environment?
- They expedite the process of resource creation
- They facilitate Kubernetes upgrades to newer versions
- They enable the development of a strategic approach, improving overall efficiency and effectiveness for operations (correct)
- They provide a user-friendly, graphical interface for managing Kubernetes


How could effective use of Kubernetes labels contribute to better cloud cost management?
- Labels can automatically downscale resources during off-peak times
- Labels can be used to identify and delete unused or idle resources, thus saving costs (correct)
- Labels can negotiate better pricing deals with cloud providers
- Labels can switch cloud providers based on current pricing



<h2>Kubernetes API</h2>

Kubernetes API - Study Tips
The video for this section is split into two parts, from a KCNA examination viewpoint it is essential that Part 1 is completed, Part 2 is optional.

The KCNA Examination focusses on the theory of the API and particular attention should be made for the following areas -

How CRD's can be used to extend the Kubernetes API
How to list resource types in a cluster
The use of --authorization-mode
The main three stages a request will pass through on its journey via the API server


Kubernetes API - the kubernetes core

Importante para: 

- Primary Interface for Users and System Components
- RESTful API
- There are many forms of interaction with the Kubernetes API

![image](https://github.com/user-attachments/assets/237b0d12-1b7f-45a7-97f9-9e832a7052a5)


![image](https://github.com/user-attachments/assets/8177df6c-fbe4-4b40-a650-ff18b187e3da)

![image](https://github.com/user-attachments/assets/a7e2a6a5-45f6-43d8-a83d-b3b2899509ca)


Admission Controller Rol

![image](https://github.com/user-attachments/assets/ee066a4e-7c57-4b2e-9a60-9b7c9ede35d2)



API Routing
1. Request Arrival
2. Route Matching (Based on URL and Method, i.e. GET POST PUT DELETE)
3. Authentication: Such as an API Key or Token
4. Authorization: Are these permissions allowed (relates to the --authorization-mode api-server parameter) if the parameter is not set, it will default to AlwaysAllow
5. Admission Controller
6. Validation
7. Request Handling
8. Response Generation
9. Response Sending


How work the authentication?
![image](https://github.com/user-attachments/assets/2ef222ba-5fbf-4910-bee8-13eacceadc1e)


Custom Resource Definition

In the Kubernetes API a resource is an endpoint that stores a collection of API objects of a certain kind. For example, the built-in pods resource contains a collection of Pod objects. A custom resource is an object that extends the Kubernetes API or allows you to introduce your own API into a project or a cluster.


kube api-server: kubernetes expone una API para poder hablar con el cluster. Nos podemos conectar por una api o por una libreria o servicios externos etc.
La API REST es la parte fundamental de Kubernetes que enlaza sus componentes. 
Todas las operaciones y comunicaciones entre componentes y comandos de usuarios externos son llamadas al API REST que maneja el servidor API. En consecuencia, todo en la plataforma Kubernetes se trata como un objeto API y tiene una entrada correspondiente en la API. Lo que basicamente quiere decir eso es que todo lo que tenemos en kubernetes: pods, services, deployments, ingress, nodos, el cluster en si se traduce hacia un objeto de k8s. Todo lo que nosotros desarrollamos o creamos corresponde hacia una entrada de su API. Nos ofrece una interfaz para podernos comunicar con el, editarlos, extenderlos, escalarlos, extraer informacion, hacer querys etc. 
![image](https://github.com/user-attachments/assets/75c7351d-6228-4390-b9af-be0f60806c47)


Importante, resvisar este video: https://www.youtube.com/watch?v=_65Md2qar14&t=2171s


![image](https://github.com/user-attachments/assets/69a0ceb9-d309-457d-a09b-a6c9e74bd2bb)





**** Contextualicemonos Importante ****

- ETCD: base de datos llave-valor. Es el cerebro critico de Kubernetes, si este elemento se elimina se borra todo el cluster. Guarda todo el estado del cluster.  Todo lo que ocurra en el cluster (si eliminamos un pod, si lo reiniciamos lo va a registrar ) Por ejemplo el status de un objeto se guardar en etcd, si una aplicacion estaba ejecutandose y paso a estado terminando ese cambio de estado se va al etcd. Todo esto pues obviamente se conecta con el api server. 

- Kube controller (o Controller Manager): es como un robot en kubernetes que se encarga de controlar todo, si necesitamos eliminar un configmap o un secreto, el se encarga de gestionar esa orden, un deployment esta fallando el se encarga de realizar todas las tareas operativas del cluster. Es basicamente donde se encuentra toda la logica de kubernetes, que hace un deployment, que hace un estafullset, que hacen todos esos componentes, que es lo que pasa detras, cada vez que yo creo un objeto o una aplicacion.  
  
- API Server (REST API): es el servidor principal, el que engloba todos los demas componentes y se encarga de su conexion y de mantener todo el cluster funcionando. Ya que el es el punto de entrada para obtener la informacion y realizar acciones. Es una API para poder hablar con el cluster. Nos podemos conectar por una api o por una libreria o servicios externos etc. Kubernetes para este API usa Open API 2.0 y 3.0 (La version actual) .

- Kube-scheduler: Es el encargado de verificar en cada uno de los nodos y saber que nodos hay disponibles (si yo tengo dos nodos disponibles, tres nodos disponibles, tengo N cantidad de nodos disponibles), identificar la cantidad especifica de pods (porque cada nodo tiene una cantidad especifica de pods desployados en el) e identificar la cantidad especifica de recursos libres que puedo utilizar y el se encarga de decidir en donde va a ir una aplicacion, si lo voy a destinar  al nodo uno que tiene un 20% de recursos utilizados o al nodo dos que tiene un 60% de recursos utilizados, obviamente tambien se encarga de buscar donde los pods pueden correr. Es el responsable de definir donde desplegamos los pods.

![image](https://github.com/user-attachments/assets/30485930-4c1e-4879-9126-ba10ee6b39ca)


Kubernetes API - Tipos

![image](https://github.com/user-attachments/assets/c89b0014-9cc6-461a-b694-a3d38cdb9b18)



Versionamiento

- No se recomienda usar alpha en PDN.
- Tampoco se recomienda usar Beta en PDN.
- Stable si es recomendable, ya fue probada y paso los diferentes fases. 


![image](https://github.com/user-attachments/assets/61fff4da-04cc-487d-bcc7-3a1c7ef757cb)


K8s API Objetos

![image](https://github.com/user-attachments/assets/4a8392cc-87d8-401d-8037-11060282229a)


K8s API Groups

![image](https://github.com/user-attachments/assets/f937854f-3148-43fd-aa39-6616ffe14ae9)

K8s Names UID

(Todos los objetos tienen nobre y toos los objetos tienen un UID)
![image](https://github.com/user-attachments/assets/d0c5e589-cd56-4cd6-87da-733d6c21bd30)




Importante y estudiar sobre el admission controller

Aqui estan los pasos en un request y como el Access the Kubernetes API trabaja: 

![image](https://github.com/user-attachments/assets/261c981b-3470-4ce3-98b9-c638bb07fba8)




<h2>Questions</h2>

What is the main purpose of the Kubernetes API?
- It allows Kubernetes to integrate with external systems
- It provides operations to create, read, update, and delete resources (Correct)
- It is used to install and update Kubernetes
- It's used for automated testing of Kubernetes


How do users typically interact with the Kubernetes API?
- Using command-line tools like kubectl and Helm (Correct)
- Directly through the API endpoints using HTTP requests
- Through the Kubernetes GUI interface
- Using third-party monitoring tools

Which component of Kubernetes uses the API to track the state of pods and nodes, and to schedule pods onto nodes?
- kube-controller-manager
- kubelet
- kube-scheduler (Correct)
- kube-apiserver

What is the role of Admission Controllers in Kubernetes API?
- They perform load balancing for the API requests
- They enforce policies and modify resources as part of processing requests (Correct)
- They handle error handling and request retrying
- They ensure the integrity of the data stored in the API

Which step does not belong in the path a request to the Kubernetes API follows?
- Response Generation
- Route Matching
- Admission Control
- Network Optimization (Correct)


If the --authorization-mode flag is not specified when starting the API server, what default mode does the Kubernetes API server use?
- RBAC
- ABAC
- Node
- AlwaysAllow (Correct)



What feature allows you to extend the Kubernetes API by defining new resource types?
- API Extensions
- Custom Resource Definitions (CRD) (Correct)
- Kubernetes Plugins
- API Modules


In the path a request to the Kubernetes API follows, which step occurs immediately after Authorization?
- Admission Control (Correct) (eso lo vemos en la imagen que esta arriba, donde dice Importante y estudiar sobre el admission controller )
- Route Matching
- Request Handling
- Validation


What would be a potential use case for an Admission Controller in a Kubernetes cluster?
- Enforcing a policy that a certain namespace doesn't exceed a given memory threshold (Correct)
- Allocating pods to nodes based on resource availability
- Managing the lifecycle of a pod
- Directly interacting with the underlying etcd database

If you want to quickly list all available API resources in your current Kubernetes cluster from the command line, which command would you use?
- kubectl api-resources (Correct)
- kubectl describe api-resources
- kubectl get api-versions
- kubectl list api-resources


The Kubernetes API is often described as a CRUD interface. What does CRUD stand for in this context?
- Create, Run, Update, Delete
- Call, Read, Update, Deploy
- Create, Read, Update, Delete (Correct)
- Copy, Read, Update, Download


What are the three crucial stages that a request to the Kubernetes API goes through in the context of security and policy enforcement?
- Authentication, Authorisation, Admission Control (Correct, de hecho podemos verlo en la misma imagen)
- Route Matching, Validation, Response Sending
- Request Arrival, Request Handling, Response Generation
- Route Matching, Authorisation, Response Sending


How does the kubectl proxy command in Kubernetes handle API server authentication?
- It bypasses the need for API server authentication
- It manually prompts the user for authentication each time
- It automatically handles authentication with the API server (Correct)
- It offloads authentication to a third-party service

For how long is the Kubernetes API guaranteed to be backward compatible following a release?
- 6 months
- 1 year (Correct)
- 2 years
- 3 years



<h2>Kubernetes RBAC</h2>

Kubernetes RBAC - Study Tips

From a KCNA examination viewpoint, only a high level knowledge of RBAC is required, for example what is the role and purpose of RBAC and how would you implement granular control. You should also be aware of Service Accounts which are covered in the Further Study section.

At a minimum, the 1st video and the Further Study guide should be reviewed.

Personally, I don't agree with skipping content and providing the bare minimum to pass an exam. RBAC is typically deemed as one of the most challenging topics to learn in Kubernetes and it is a favourite with interviewees in most Kubernetes job interviews.

A lot of content on RBAC is fragmented and doesn't cover the specifics or mechanics of how RBAC is actually working on a newly installed Cluster.

This 3 part video series is an extensive look at RBAC from the ground up and by the end of it, you'll be able confidently use and support RBAC. You'll also gain knowledge of advanced usage with Service Accounts in the Further Study section.

If your focus in the KCNA examination then use these videos and further study sections accordingly and where required, treat them as available resources for consumption later.




RBAC

Significa Control de acceso basado en roles.

<h3>Expectations for Users and Groups</h3>

- Kubernetes does not manage user and group accounts!
- Kubernetes expects certificates to be created and authorised by the certificate authority
- If a certificate is signed by the Certificate Authority's Private Key and it has a user (CN) and a group (0) - Kubernetes respects this as a valid user and group

![image](https://github.com/user-attachments/assets/ff361ed8-15bd-49fa-9eb3-3b77fa1e92b8)

Concepts in RBAC:

Users: These are the individuals or applications that interact with the Kubernetes cluster. They could be administrators managing the cluster, developers deploying applications, or automated systems interacting with the cluster. Users are not managed by Kubernetes and it is assumed that they are managed externally. In Kubernetes, users are represented by strings, which can be simple like "alice", or more complex like "alice@example.com".

Groups: Groups are also managed outside of Kubernetes. A group represents multiple users, and it's a way to attach a set of users to a certain set of permissions. When permissions are given to a group, all users that are part of that group receive those permissions.

ServiceAccounts: Used by applications running inside the cluster itself, not by humans. Unlike Users and Groups, ServiceAccounts are Kubernetes objects are managed by Kubernetes. They are tied to a specific namespace, and their permissions are scoped to that namespace unless additional permissions are given. ServiceAccounts are used to give an application running in a pod the necessary permissions to interact with the Kubernetes API.

![image](https://github.com/user-attachments/assets/2a458c29-2552-4eaf-a46f-f1262d7e7b3d)


Commands:

<h4>coomand: kubectl get clusterrolebindings -o wide</h4>: 
El comando kubectl get clusterrolebindings -o wide se utiliza en Kubernetes para listar todos los ClusterRoleBindings en el clúster, y la opción -o wide amplía la salida con información adicional.

Explicación del comando:
kubectl get: Este es el comando general utilizado para obtener información sobre los recursos de Kubernetes. Puedes utilizarlo para obtener detalles de diferentes tipos de recursos (pods, services, deployments, etc.).

clusterrolebindings: Especifica que el recurso que deseas obtener es de tipo ClusterRoleBinding. Los ClusterRoleBindings se utilizan para asociar un ClusterRole (un conjunto de permisos) con un usuario, grupo o cuenta de servicio en un clúster de Kubernetes, lo que permite que el sujeto especificado tenga los permisos definidos en ese rol.

-o wide: Esta opción modifica el formato de la salida para incluir información adicional. En este caso, agrega columnas extra a la salida para proporcionar más detalles sobre cada ClusterRoleBinding, como el nombre del sujeto (usuario, grupo o cuenta de servicio), el nombre del rol al que se hace referencia y las acciones asociadas.





Estudiar los siguientes conceptos:

Eso es sacado de: https://kubernetes.io/docs/concepts/security/rbac-good-practices/

Kubernetes RBAC is a key security control to ensure that cluster users and workloads have only the access to resources required to execute their roles. It is important to ensure that, when designing permissions for cluster users, the cluster administrator understands the areas where privilege escalation could occur, to reduce the risk of excessive access leading to security incidents.

The good practices laid out here should be read in conjunction with the general RBAC documentation.

General good practice
Least privilege
Ideally, minimal RBAC rights should be assigned to users and service accounts. Only permissions explicitly required for their operation should be used. While each cluster will be different, some general rules that can be applied are :

Assign permissions at the namespace level where possible. Use RoleBindings as opposed to ClusterRoleBindings to give users rights only within a specific namespace.
Avoid providing wildcard permissions when possible, especially to all resources. As Kubernetes is an extensible system, providing wildcard access gives rights not just to all object types that currently exist in the cluster, but also to all object types which are created in the future.
Administrators should not use cluster-admin accounts except where specifically needed. Providing a low privileged account with impersonation rights can avoid accidental modification of cluster resources.
Avoid adding users to the system:masters group. Any user who is a member of this group bypasses all RBAC rights checks and will always have unrestricted superuser access, which cannot be revoked by removing RoleBindings or ClusterRoleBindings. As an aside, if a cluster is using an authorization webhook, membership of this group also bypasses that webhook (requests from users who are members of that group are never sent to the webhook)
Minimize distribution of privileged tokens
Ideally, pods shouldn't be assigned service accounts that have been granted powerful permissions (for example, any of the rights listed under privilege escalation risks). In cases where a workload requires powerful permissions, consider the following practices:

Limit the number of nodes running powerful pods. Ensure that any DaemonSets you run are necessary and are run with least privilege to limit the blast radius of container escapes.
Avoid running powerful pods alongside untrusted or publicly-exposed ones. Consider using Taints and Toleration, NodeAffinity, or PodAntiAffinity to ensure pods don't run alongside untrusted or less-trusted Pods. Pay special attention to situations where less-trustworthy Pods are not meeting the Restricted Pod Security Standard.
Hardening
Kubernetes defaults to providing access which may not be required in every cluster. Reviewing the RBAC rights provided by default can provide opportunities for security hardening. In general, changes should not be made to rights provided to system: accounts some options to harden cluster rights exist:

Review bindings for the system:unauthenticated group and remove them where possible, as this gives access to anyone who can contact the API server at a network level.
Avoid the default auto-mounting of service account tokens by setting automountServiceAccountToken: false. For more details, see using default service account token. Setting this value for a Pod will overwrite the service account setting, workloads which require service account tokens can still mount them.
Periodic review
It is vital to periodically review the Kubernetes RBAC settings for redundant entries and possible privilege escalations. If an attacker is able to create a user account with the same name as a deleted user, they can automatically inherit all the rights of the deleted user, especially the rights assigned to that user.



Kubernetes RBAC - privilege escalation risks
Within Kubernetes RBAC there are a number of privileges which, if granted, can allow a user or a service account to escalate their privileges in the cluster or affect systems outside the cluster.

This section is intended to provide visibility of the areas where cluster operators should take care, to ensure that they do not inadvertently allow for more access to clusters than intended.

Listing secrets
It is generally clear that allowing get access on Secrets will allow a user to read their contents. It is also important to note that list and watch access also effectively allow for users to reveal the Secret contents. For example, when a List response is returned (for example, via kubectl get secrets -A -o yaml), the response includes the contents of all Secrets.

Workload creation
Permission to create workloads (either Pods, or workload resources that manage Pods) in a namespace implicitly grants access to many other resources in that namespace, such as Secrets, ConfigMaps, and PersistentVolumes that can be mounted in Pods. Additionally, since Pods can run as any ServiceAccount, granting permission to create workloads also implicitly grants the API access levels of any service account in that namespace.

Users who can run privileged Pods can use that access to gain node access and potentially to further elevate their privileges. Where you do not fully trust a user or other principal with the ability to create suitably secure and isolated Pods, you should enforce either the Baseline or Restricted Pod Security Standard. You can use Pod Security admission or other (third party) mechanisms to implement that enforcement.

For these reasons, namespaces should be used to separate resources requiring different levels of trust or tenancy. It is still considered best practice to follow least privilege principles and assign the minimum set of permissions, but boundaries within a namespace should be considered weak.

Persistent volume creation
If someone - or some application - is allowed to create arbitrary PersistentVolumes, that access includes the creation of hostPath volumes, which then means that a Pod would get access to the underlying host filesystem(s) on the associated node. Granting that ability is a security risk.

There are many ways a container with unrestricted access to the host filesystem can escalate privileges, including reading data from other containers, and abusing the credentials of system services, such as Kubelet.

You should only allow access to create PersistentVolume objects for:

Users (cluster operators) that need this access for their work, and who you trust.
The Kubernetes control plane components which creates PersistentVolumes based on PersistentVolumeClaims that are configured for automatic provisioning. This is usually setup by the Kubernetes provider or by the operator when installing a CSI driver.
Where access to persistent storage is required trusted administrators should create PersistentVolumes, and constrained users should use PersistentVolumeClaims to access that storage.

Access to proxy subresource of Nodes
Users with access to the proxy sub-resource of node objects have rights to the Kubelet API, which allows for command execution on every pod on the node(s) to which they have rights. This access bypasses audit logging and admission control, so care should be taken before granting rights to this resource.

Escalate verb
Generally, the RBAC system prevents users from creating clusterroles with more rights than the user possesses. The exception to this is the escalate verb. As noted in the RBAC documentation, users with this right can effectively escalate their privileges.

Bind verb
Similar to the escalate verb, granting users this right allows for the bypass of Kubernetes in-built protections against privilege escalation, allowing users to create bindings to roles with rights they do not already have.

Impersonate verb
This verb allows users to impersonate and gain the rights of other users in the cluster. Care should be taken when granting it, to ensure that excessive permissions cannot be gained via one of the impersonated accounts.

CSRs and certificate issuing
The CSR API allows for users with create rights to CSRs and update rights on certificatesigningrequests/approval where the signer is kubernetes.io/kube-apiserver-client to create new client certificates which allow users to authenticate to the cluster. Those client certificates can have arbitrary names including duplicates of Kubernetes system components. This will effectively allow for privilege escalation.

Token request
Users with create rights on serviceaccounts/token can create TokenRequests to issue tokens for existing service accounts.

Control admission webhooks
Users with control over validatingwebhookconfigurations or mutatingwebhookconfigurations can control webhooks that can read any object admitted to the cluster, and in the case of mutating webhooks, also mutate admitted objects.

Namespace modification
Users who can perform patch operations on Namespace objects (through a namespaced RoleBinding to a Role with that access) can modify labels on that namespace. In clusters where Pod Security Admission is used, this may allow a user to configure the namespace for a more permissive policy than intended by the administrators. For clusters where NetworkPolicy is used, users may be set labels that indirectly allow access to services that an administrator did not intend to allow.

Kubernetes RBAC - denial of service risks 
Object creation denial-of-service
Users who have rights to create objects in a cluster may be able to create sufficient large objects to create a denial of service condition either based on the size or number of objects, as discussed in etcd used by Kubernetes is vulnerable to OOM attack. This may be specifically relevant in multi-tenant clusters if semi-trusted or untrusted users are allowed limited access to a system.

One option for mitigation of this issue would be to use resource quotas to limit the quantity of objects which can be created.



***** Importante ****
Leer el siguiente post: https://medium.com/@muppedaanvesh/a-hand-on-guide-to-kubernetes-rbac-with-a-user-creation-%EF%B8%8F-1ad9aa3cafb1
El RBAC tambien lo explican en este video: https://www.youtube.com/watch?v=iE9Qb8dHqWI
Charla importante: https://www.youtube.com/watch?v=yFSlK_7Atco
https://www.youtube.com/watch?v=MGCF6slXG0w

Secuence Diagram
![image](https://github.com/user-attachments/assets/6ee36259-cd95-4a52-bdb6-b5ee0ee79995)


<h3>ClusterRole y ClusterRoleBinding</h3>

- ClusterRole: A ClusterRole is a non-namespaced resource, meaning it applies to the entire cluster and it allows us to set permissions on resources across all namespaces. Remember, a ClusterRole is Non Namespaced

Crear un cluster role: <code>kubectl create clusterrole cluster-superhero --verb='*' --resource='*'</code>

kubectl: Esta es la herramienta de línea de comandos de Kubernetes. Es como el "mando a distancia" que utilizamos para interactuar con nuestros clústeres de Kubernetes.
create: Este verbo le indica a kubectl que queremos crear un nuevo recurso.
clusterrole: El tipo de recurso que vamos a crear es un "ClusterRole". Un ClusterRole define un conjunto de permisos que se pueden aplicar a cualquier espacio de nombres o a todo el clúster.
cluster-superhero: Este es el nombre que le hemos dado a nuestro nuevo ClusterRole. Puedes elegir cualquier nombre que quieras, pero es recomendable que sea descriptivo.
--verb='*': Esto significa que el ClusterRole tendrá permiso para realizar cualquier acción (verbo) sobre los recursos. El asterisco (*) es un comodín que representa todas las posibles acciones.
--resource='*': Similar al anterior, esto significa que el ClusterRole tendrá permiso sobre todos los recursos (nombres de objetos) del clúster.






- ClusterRoleBinding: Binds a ClusterRole to a Service Account, Group and/or Users

Crear un ClusterRoleBinding: <code>kubectl create clusterrolebinding cluster-superhero --clusterrole=cluster-superhero --group=cluster-superheroes</code>


kubectl create: This part tells Kubernetes to create a new resource.
clusterrolebinding cluster-superhero: This specifies that we're creating a ClusterRoleBinding named "cluster-superhero".
--clusterrole=cluster-superhero: This argument links the ClusterRoleBinding to the ClusterRole named "cluster-superhero". This ClusterRole must already exist.
--group=cluster-superheroes: This argument specifies that the permissions defined in the "cluster-superhero" ClusterRole will be granted to the group "cluster-superheroes". This group must be defined in your Kubernetes configuration, often in a RBAC ConfigMap or a ServiceAccount.



Luego hacemos esto: <code>kubectl auth can-i '*' '*'</code>
<code>kubectl auth can-i '*' '*' --as-group="cluster-superheroes" --as="batman"</code>
<code>kubectl auth can-i '*' '*' --as-group="cluster-superheroes" --as="batman"</code>

El comando kubectl auth can-i '*' '*' es una herramienta poderosa para verificar los permisos en Kubernetes, pero debe utilizarse con precaución. Recuerda que otorgar permisos excesivos puede comprometer la seguridad de tu clúster.


y en realidad hacemos algo como esto:

![image](https://github.com/user-attachments/assets/af356c4b-3bfa-45e8-95ef-66b0926f03e4)



<h3>ClusterRole y ClusterRoleBinding en Kubernetes</h3>

<p>En Kubernetes, el control de acceso basado en roles (RBAC) es fundamental para gestionar los permisos de los usuarios y servicios. Los ClusterRoles y ClusterRoleBindings son dos de los componentes clave de este sistema.</p>

  <h3>ClusterRole</h3>
    <p>Un ClusterRole define un conjunto de permisos que se pueden aplicar a cualquier espacio de nombres o a todo el clúster.</p>
    <ul>
        <li><strong>Alcance:</strong> Cluster-wide</li>
        <li><strong>Funcionalidad:</strong> Define qué acciones (verbos) se pueden realizar sobre qué tipos de recursos (kinds).</li>
        <li><strong>Ejemplo:</strong> Un ClusterRole podría otorgar permiso para crear, listar y eliminar pods en todos los espacios de nombres.</li>
    </ul>

   <h3>ClusterRoleBinding</h3>
    <p>Un ClusterRoleBinding vincula un ClusterRole específico a un usuario o grupo de servicio.</p>
    <ul>
        <li><strong>Función:</strong> Establece quién puede utilizar los permisos definidos en un ClusterRole.</li>
        <li><strong>Alcance:</strong> También es un recurso de alcance cluster-wide.</li>
        <li><strong>Ejemplo:</strong> Un ClusterRoleBinding podría asignar el ClusterRole mencionado anteriormente a un usuario llamado "admin", otorgándole los permisos para gestionar pods en todo el clúster.</li>
    </ul>

   <h3>Tabla Comparativa</h3>
    <table>
        <tr>
            <th>Característica</th>
            <th>ClusterRole</th>
            <th>ClusterRoleBinding</th>
        </tr>
        <tr>
            <td>Definición</td>
            <td>Conjunto de permisos</td>
            <td>Vincula un ClusterRole a un sujeto</td>
        </tr>
        <tr>
            <td>Alcance</td>
            <td>Cluster-wide</td>
            <td>Cluster-wide</td>
        </tr>
        <tr>
            <td>Función</td>
            <td>Define qué se puede hacer</td>
            <td>Asigna permisos a usuarios o grupos</td>
        </tr>
        <tr>
            <td>Ejemplo</td>
            <td>Permitir crear pods en todos los namespaces</td>
            <td>Otorgar el permiso de crear pods a un usuario específico</td>
        </tr>
    </table>

   <h3>¿Cuándo usar cada uno?</h3>
    <ul>
        <li><strong>ClusterRole:</strong>
            <ul>
                <li>Cuando necesitas definir permisos que se aplicarán a múltiples espacios de nombres o a todo el clúster.</li>
                <li>Para crear roles reutilizables que puedan ser asignados a diferentes sujetos.</li>
            </ul>
        </li>
        <li><strong>ClusterRoleBinding:</strong>
            <ul>
                <li>Para asignar los permisos definidos en un ClusterRole a usuarios o grupos específicos.</li>
                <li>Cuando quieres otorgar acceso a nivel de clúster a ciertos recursos.</li>
            </ul>
        </li>
    </ul>

   <p><strong>En resumen:</strong> Los ClusterRoles definen los permisos, mientras que los ClusterRoleBindings asignan esos permisos a los usuarios o grupos. Ambos son esenciales para implementar una estrategia de seguridad sólida en Kubernetes.</p>

Proceso de RBAC

![image](https://github.com/user-attachments/assets/9dad7bab-b752-44ef-bf41-6a8f203a8a81)


<h3>ClusterRole/Binding vs Role/Binding</h3>

![image](https://github.com/user-attachments/assets/246a8e76-b656-40e7-a4be-b7acc8ddbc40)


Revisemos esto, por ejemplo:

![image](https://github.com/user-attachments/assets/601e3a25-7633-4174-8b92-9a4401a7f177)


<h2>Questions RBAC</h2>

What is the purpose of Role Based Access Control (RBAC) in Kubernetes?
- Managing User Interface
- Assigning specific roles to users and groups (correct)
- Creating new Kubernetes Clusters
- Configuring Network Policies


What does the kubeconfig file contain?
- Cluster details and user information (correct)
- Only cluster details
- Only user information
- RBAC configurations


What is the purpose of Certificate Authority (CA) in Kubernetes?
- To verify user identity
- To create and verify certificates in the cluster (correct)
- To encode and decode base64 data
- To configure RBAC

Explanation: El Certificate Authority (CA) en Kubernetes se encarga de la creación, gestión y verificación de certificados digitales dentro del clúster. Estos certificados son utilizados para establecer una comunicación segura, autenticada y cifrada entre los componentes del clúster, como el servidor API y los nodos, así como para autenticar a los usuarios y servicios.


How are Users and Groups typically managed in Kubernetes?
- Managed by Kubernetes directly
- Managed externally  (correct)
- Managed by ServiceAccounts
- Managed by the kubeconfig file

Explanation: En Kubernetes, los usuarios y grupos no son gestionados directamente por Kubernetes. En lugar de ello, la gestión de usuarios y grupos suele ser realizada externamente, por ejemplo, a través de un sistema de identidad como LDAP, Active Directory, o proveedores de identidad basados en OAuth, OpenID Connect (OIDC) o incluso certificados. Kubernetes en sí no tiene un sistema de gestión de usuarios incorporado; más bien, se integra con sistemas de autenticación externos para verificar la identidad de los usuarios.


What does a ClusterRole in Kubernetes define?
- Permissions on resources within a namespace
- Permissions on resources across cluster resources (correct)
- The role of a cluster administrator
- The configurations for a Kubernetes Cluster


Explanation: Mirar en la tablita de comparaciones.


What does the command kubectl auth can-i * * check?
- If Kubernetes is properly installed
- If the user has permissions to perform any action on any resource (correct)
- If RBAC is enabled
- If the user is part of a specific group



How are permissions assigned to a user in Kubernetes using RBAC?
- Directly assigning permissions to the user
- Through the user’s membership or group membership assigned by a ClusterRoleBinding (correct)
- Via the kubeconfig file
- By modifying the Kubernetes API server


Explanation: En Kubernetes, la gestión de permisos a través de RBAC (Role-Based Access Control) no implica asignar permisos directamente a un usuario. En su lugar, se asignan roles a los usuarios mediante bindings (vinculaciones). Los usuarios y grupos no son gestionados directamente dentro de Kubernetes, sino que se les asignan permisos a través de un RoleBinding o ClusterRoleBinding que asocia un Role o ClusterRole a un usuario o un grupo de usuarios.


Which command is used to create an RSA private key?
- openssl genrsa -out user.key 4096 (correct)
- openssl rsa -in user.key -outform PEM
- kubectl create rsa user.key
- openssl create -rsa user.key 4096

Explanation: El comando openssl genrsa se utiliza para generar una clave privada RSA. Este comando genera una clave privada en formato PEM, que luego se puede usar para crear certificados o autenticarse en sistemas que requieran RSA. El número 4096 especifica el tamaño de la clave en bits (en este caso, una clave de 4096 bits).

Me pregunte por que de ese numero? es obligatorio, pero es el tamaño en bits, esta es la respuesta: Sí, el número 4096 puede cambiar. Este número representa el tamaño de la clave RSA en bits. En general, cuanto mayor es el tamaño de la clave, más segura es, pero también más costosa es en términos de tiempo de procesamiento. Los tamaños comunes para las claves RSA son 2048 bits, 3072 bits y 4096 bits, aunque también es posible usar otros tamaños según las necesidades de seguridad y el rendimiento.


What does the "O" stand for in the subject line of a Kubernetes certificate?
- Origin
- Organization (Correct)
- Operator
- Owner


How is a new user, such as "batman", associated with a group in Kubernetes RBAC?
- By adding the user to a Group object in Kubernetes
- Through the "O" field in the certificate subject (Correct)
- By listing the user under the group in KUBECONFIG
- Through a User-Group Binding in Kubernetes

Explanation: En Kubernetes RBAC (Role-Based Access Control), los usuarios no se gestionan directamente dentro del clúster de Kubernetes. Sin embargo, cuando un usuario se autentica en el clúster (por ejemplo, mediante certificados, tokens o proveedores de identidad como OIDC), puede ser asociado a un grupo o rol. Esta asociación a menudo se realiza mediante el campo "O" (Organizational Unit) dentro del subject de un certificado, que puede ser interpretado como un grupo en el contexto de RBAC.


What does the "CN" stand for in the subject line of a Kubernetes certificate?
- Common Node
- Certificate Number
- Common Name  (Correct)
- Connection Node

Explanation: El "CN" en la línea de asunto de un certificado X.509 (como los que se utilizan en Kubernetes para la autenticación) significa "Common Name" (Nombre Común). El "Common Name" es un campo que generalmente se usa para identificar de manera única al sujeto del certificado, y es comúnmente utilizado para especificar el nombre de la entidad o el servicio al que pertenece el certificado.

openssl req -new -newkey rsa:2048 -days 365 -nodes -keyout batman.key -out batman.crt -subj "/CN=batman/O=Kubernetes/L=Gotham"

Desglose del comando:
openssl req: Comando para generar una solicitud de certificado (CSR) y un certificado auto-firmado.
-new: Indica que estamos generando una nueva solicitud de certificado.
-newkey rsa:2048: Genera una nueva clave privada con el algoritmo RSA y un tamaño de 2048 bits.
-days 365: El certificado será válido por 365 días.
-nodes: Significa que la clave privada no estará cifrada (sin passphrase).
-keyout batman.key: Especifica el archivo donde se guardará la clave privada (en este caso, batman.key).
-out batman.crt: Especifica el archivo donde se guardará el certificado (en este caso, batman.crt).
-subj "/CN=batman/O=Kubernetes/L=Gotham": Define el DN (Distinguished Name) del certificado, especificando:
CN=batman: El "Common Name" es batman (es el nombre del usuario o entidad).
O=Kubernetes: La organización es Kubernetes.
L=Gotham: La localidad es Gotham.
¿Qué hace este comando?
Este comando genera un certificado auto-firmado con una clave privada RSA de 2048 bits y lo guarda en los archivos batman.key (clave privada) y batman.crt (certificado). El CN del certificado será batman, lo que indica que este certificado está asociado con el usuario "batman". Este certificado podría ser utilizado, por ejemplo, para autenticarse en un clúster de Kubernetes si la autenticación está basada en certificados.


Which of the following statements accurately describes the difference between Roles and ClusterRoles in Kubernetes?
- Roles can only be applied at the cluster level, whereas ClusterRoles can be applied at both the cluster and namespace levels
- ClusterRoles are used to define permissions at the cluster level, while Roles are used to define permissions at the namespace level (Correct)
- Roles and ClusterRoles are interchangeable, and there is no significant difference between them
- ClusterRoles can only be applied to nodes, while Roles can be applied to pods and services

Explanation: ahi esta en la tabla.


In Kubernetes, if a Pod is deployed without an explicitly assigned Service Account, which Service Account is automatically assigned?
- admin
- kube-system
- default (Correct)
- node

Explanation: En Kubernetes, si un Pod es desplegado sin un Service Account explícitamente asignado, Kubernetes le asigna automáticamente el Service Account llamado default.
Cada namespace en Kubernetes tiene un Service Account llamado default, y si no se especifica uno al crear un pod, Kubernetes utiliza este default para las operaciones de autenticación dentro del clúster.


<h2>Kubernetes Scheduler and NodeName</h2>

Kubernetes Scheduler and NodeName - Study Tips
For the KCNA qualification, a basic knowledge and understanding of the role of the scheduler is required. Particular attention should be applied to the use of nodeName as well as nodeSelector and the mechanism of labels that the nodeSelector makes us of (nodeSelector is an addition covered in the Further Study addendum).


Kube Scheduler
Schedule Applications in the form of Pods to run on various nodes.

![image](https://github.com/user-attachments/assets/f064be04-f4a0-4083-bfad-34cc063d1f82)

![image](https://github.com/user-attachments/assets/64a0b377-a7cb-47a6-bd97-98ca58b198d4)


Interaction and processes

1. Pod is Created - Kube-Scheduler will take this on as a task to complete
2. Checks available resources and identifies the best node to run on
3. Pod Placement - Assigns the Pod to a Node
4. Kubelet running on a chosen node starts the Pod



***Importante***
Averiguar sobre el objeto binding en kubernetes. (esta inquietud se resuelve a continuacion)

![image](https://github.com/user-attachments/assets/f040a4fe-6bff-4d5f-88db-e5f8b0e69df9)

En Kubernetes, el Binding Object es un recurso utilizado para vincular un Pod a un Nodo específico. Este objeto se usa principalmente en el contexto de la programación de Pods, donde el Scheduler asigna un Pod a un Nodo y luego se crea el Binding para que el Pod se ejecute en ese Nodo determinado.

El Binding Object no se usa directamente por los usuarios en la mayoría de los casos, ya que es gestionado internamente por Kubernetes, pero se puede utilizar en situaciones donde se necesite asignar un Pod a un Nodo específico de manera explícita.



3 Main Sets of operation

- Filtering: If a Pod requires more memory than a certain node has available, that node would be filtered out
- Scoring: The Scheduler scores the individual nodes to find the most appropriate node
- Binding: A Pod is bound to a Node using the Binding Object

![image](https://github.com/user-attachments/assets/a3ff7469-b087-4d7e-9d63-c5fb3f4ae7e1)


SchedulerName


En Kubernetes, el SchedulerName es un atributo que se utiliza para especificar qué Scheduler se encargará de asignar un Pod a un nodo específico dentro de un clúster.

Selección del programador: Al especificar un SchedulerName en una definición de Pod, estás indicando a Kubernetes que utilice un programador específico para ese Pod en lugar del programador predeterminado (kube-scheduler).
Personalización de la programación: Esto te permite crear programas personalizados que se adapten a las necesidades específicas de tu aplicación. Por ejemplo, puedes crear un programador que priorice los Pods de una aplicación crítica o que evite colocar ciertos Pods en nodos específicos. Esto quiere decir que podemos crear nuestro Scheduler custom propio y usarlo en nuestro archivo .yaml para las operaciones. 

Ejemplo de uso:

    apiVersion: v1
    kind: Pod
    metadata:
      name: my-pod
    spec:
      schedulerName: my-custom-scheduler
      containers:
      - name: my-container
        image: my-image

![image](https://github.com/user-attachments/assets/e3f25c0f-f8b7-4cf2-9ab6-1c172e7a9441)

Kubernetes Scheduler and NodeName - Further Study
It is also possible to use a more targeted approach than NodeName through the use of NodeSelectors, the approach is similar but, instead of a direct node we will make use of Kubernetes labels to identify our desired target.

For awareness as a comparison. View the available node labels as follows -

kubectl describe node/worker-1 | more

Name:               worker-1
Roles:              <none>
Labels:             beta.kubernetes.io/arch=arm64
                    beta.kubernetes.io/instance-type=k3s
                    beta.kubernetes.io/os=linux
                    kubernetes.io/arch=arm64
                    kubernetes.io/hostname=worker-1
                    kubernetes.io/os=linux
                    node.kubernetes.io/instance-type=k3s
And then, you can use the nodeSelector option to select specific nodes through the use of labels -

  nginx_scheduler.yaml
  
     apiVersion: v1
     kind: Pod
     metadata:
       creationTimestamp: null
       labels:
         run: nginx
       name: nginx
     spec:
       nodeSelector:
         kubernetes.io/hostname: worker-1
       containers:
       - image: nginx
         name: nginx
         resources: {}
       dnsPolicy: ClusterFirst
       restartPolicy: Always
     status: {}


<h2>Questions Scheduler </h2>

What is the primary function of the kube-scheduler in Kubernetes?
- To manage the lifecycle of containers
- To schedule applications to run on various nodes (Correct)
- To monitor the health of pods
- To allocate storage resources to pods


Which of the following is NOT one of the main operations employed by the Kube-Scheduler?
- Filtering
- Scoring
- Binding
- Replicating (Correct)


What happens during the "Filtering" stage of the Kube-Scheduler's process?
- It assigns the pod to the chosen node
- It restarts pods that have failed
- It finds nodes that meet the scheduling requirements (Correct)
- It calculates the resource usage of each node

What is the purpose of the schedulerName field in a pod’s specification
- To name the pod
- To assign the pod to a specific namespace
- To specify which scheduler should dispatch the pod (Correct)
- To define the restart policy of the pod


Which language is most typically used for creating a custom scheduler in Kubernetes?
- Python
- JavaScript
- Golang  (Correct)
- Ruby

What does the nodeName field in a pod specification indicate?
- The name of the pod
- The specific node to schedule the pod onto (Correct)
- The name of the node where the pod is currently running
- The label of the node

What is the role of the nodeSelector field in a pod's specification?
- To automatically select the best node for the pod
- To define node-specific environment variables
- To specify labels that must match a node's labels for the pod to be scheduled on that node (Correct)
- To create a new node for the pod



<h2>Kubernetes Storage</h2>

Kubernetes Storage - Study Tips
For the KCNA Examination, as well as having top level knowledge there is a heavy emphasis on the internals and specifics of the Kubernetes Storage subsystem. Please pay attention to the following areas -

What is Ephemeral Storage
What is Persistent Storage
Examples of CNCF Graduated Storage Solution(s)
Retain Policies



Ephemeral Storage

Imagina el almacenamiento efímero como un borrador que se borra al final de una clase. Es un espacio de almacenamiento temporal que se asigna a un pod (un grupo de contenedores) en Kubernetes. Una vez que el pod se detiene o se elimina, los datos almacenados en este tipo de volumen se pierden.

Características Clave:

Temporal: Los datos no persisten más allá del ciclo de vida del pod.
Local: El almacenamiento suele estar ligado al nodo donde se ejecuta el pod.
Rápido: Generalmente ofrece un alto rendimiento debido a su naturaleza local.
Ideal para:
Datos de estado que no necesitan ser persistentes, como logs temporales o archivos de configuración que se regeneran.
Aplicaciones que generan datos de forma constante pero no requieren archivarlos.
Cachés locales para mejorar el rendimiento de las aplicaciones.
¿Por qué usar almacenamiento efímero?

Simplicidad: No requiere configuración compleja de volúmenes persistentes.
Costo: Puede ser más económico que el almacenamiento persistente, especialmente para cargas de trabajo que no requieren alta durabilidad.
Rendimiento: El acceso local suele ser más rápido que el acceso a almacenamiento remoto.
¿Cuándo no usar almacenamiento efímero?

Datos persistentes: Si tus datos necesitan ser retenidos más allá del ciclo de vida del pod, debes usar volúmenes persistentes.
Alta disponibilidad: Si requieres que tus datos estén disponibles en múltiples nodos, el almacenamiento efímero no es la mejor opción.
Ejemplo de uso:

Imagina una aplicación web que procesa archivos de registro. Los archivos de registro se generan constantemente y se almacenan en un volumen efímero. Si el pod se reinicia, los nuevos archivos de registro se sobrescribirán en el volumen vacío.

En resumen:

El almacenamiento efímero es una herramienta útil en Kubernetes para manejar datos temporales y mejorar el rendimiento de las aplicaciones. Sin embargo, es esencial comprender sus limitaciones y elegir el tipo de almacenamiento adecuado para cada caso de uso.

Sobre los pods: pods use ephemeral local storage for scratch space, caching, and logs. Pods can be evicted due to other pods filling the local storage, after which new pods are not admitted until sufficient storage has been reclaimed.

![image](https://github.com/user-attachments/assets/126a42e4-81e4-43bf-8a7e-1faa86b27844)


<h3>EmptyDir</h3>

An emptyDir volume is first created when a Pod is assigned to a node, and exists as long as that Pod is running on that node. As the name says, the emptyDir volume is initially empty. All containers in the Pod can read and write the same files in the emptyDir volume, though that volume can be mounted at the same or different paths in each container. When a Pod is removed from a node for any reason, the data in the emptyDir is deleted permanently.
Note: A container crashing does not remove a Pod from a node. The data in an emptyDir volume is safe across container crashes.
Some uses for an emptyDir are:
• scratch space, such as for a disk-based merge sort
• checkpointing a long computation for recovery from crashes
• holding files that a content-manager container fetches while a webserver container serves the data
The emptyDir.medium field controls where emptyDir volumes are stored. By default emptyDir volumes are stored on whatever medium that backs the node such as disk, SSD, or network storage, depending on your environment. If you set the emptyDir.medium field to "Memory", Kubernetes mounts a tmpfs (RAM-backed filesystem) for you instead. While tmpfs is very fast, be aware that unlike disks, tmpfs is cleared on node reboot and any files you write count against your container's memory limit.

emptyDir configuration example

    apiVersion: v1
    kind: Pod
    metadata: null
    name: test-pd
    spec: null
    containers:
      - image: registry.k8s.io/test-webserver
        name: test-container
        volumeMounts:
          - mountPath: /cache
            name: cache-volume
            volumes:
              - name: cache-volume
                emptyDir: null
                sizeLimit: 500Mi


Otro ejemplo: 

    apiVersion: v1
    kind: Pod
    metadata:
      creationTimestamp: null
      labels:
        run: ubuntu
      name: ubuntu-test
    spec:
      containers:
      - command:
          - sleep
          - infinity
        image: ubuntu
        name: ubuntu
        resources: {}
        volumeMounts:
        - mountPath: /cache
          name: cache-volume
      dnsPolicy: ClusterFirst
      restartPolicy: Always
      volumes:
      - name: cache-volume
        emptyDir: {
          medium: Memory
        }   
    status: {}


![image](https://github.com/user-attachments/assets/18b302c4-08e3-43ba-a58f-2dd5f4727c9e)


Persistence Storage

Persistent Volumes (PV)
Definition: Persistent Volumes are storage resources provisioned in a Kubernetes cluster, managed by the cluster administrator. They provide an abstraction layer over physical storage devices, allowing users to access storage without needing to know the underlying infrastructure details.

Available Options:
Capacity: Specifies the size of the volume.
Access Modes: Defines how the volume can be accessed. Below are the available options.
1. ReadWriteOnce: Can be mounted as read-write by a single node.
2. ReadOnlyMany: Can be mounted as read-only by multiple nodes.
3. ReadWriteMany: Can be mounted as read-write by multiple nodes.
Storage Class Name: Associates the PV with a specific Storage Class.
Volume Mode: Determines whether the volume is mounted as a filesystem or block device.
Persistent Volume Reclaim Policy: Determines what happens to the PV’s resources when released.
Mount Options: Additional options to be passed to the mount command.
Example: Manual PV Creation
apiVersion: v1
kind: PersistentVolume
metadata:
  name: example-pv
spec:
  capacity:
    storage: 10Gi
  accessModes:
    - ReadWriteOnce
  storageClassName: manual
  persistentVolumeReclaimPolicy: Retain


![image](https://github.com/user-attachments/assets/633c5297-3a8a-4ef3-be52-7e7cc42f985b)


***Importante y Obligatorio*** 
Leer el siguiente articulo:  https://medium.com/@muppedaanvesh/a-hand-on-guide-to-kubernetes-volumes-%EF%B8%8F-b59d4d4e347f


****Importante Tambien (Que no se nos olvide)***

Hay una herramienta Open-Source, que fue concebida en la Cloud Native Computing Foundation para el Cloud-Native Storage for Kubernetes Production ready management for File, Block and Object Storage Llamada <strong>Rook</strong>


What is Rook?

Storage Operators for Kubernetes
Rook turns distributed storage systems into self-managing, self-scaling, self-healing storage services. It automates the tasks of a storage administrator: deployment, bootstrapping, configuration, provisioning, scaling, upgrading, migration, disaster recovery, monitoring, and resource management.

Rook uses the power of the Kubernetes platform to deliver its services via a Kubernetes Operator for Ceph.


Commands

- kubectl get storageclass: El comando kubectl get storageclass se utiliza en Kubernetes para listar las StorageClasses disponibles en el clúster. Las StorageClasses definen los diferentes tipos de almacenamiento que pueden ser utilizados para aprovisionar volúmenes persistentes (PVs) en Kubernetes.

¿Qué es una StorageClass?
En Kubernetes, una StorageClass es un recurso que describe los diferentes tipos de almacenamiento que un clúster puede utilizar. Una StorageClass define la manera en que los volúmenes persistentes (PVs) son creados y gestionados. Esto incluye detalles como el tipo de almacenamiento (por ejemplo, SSD, HDD, almacenamiento en la nube), políticas de aprovisionamiento, y parámetros específicos relacionados con el proveedor de almacenamiento.

En otras palabras, las StorageClasses permiten a los usuarios especificar cómo deben ser aprovisionados los volúmenes persistentes cuando crean un PersistentVolumeClaim (PVC). De esta forma, Kubernetes puede crear automáticamente el almacenamiento adecuado según las necesidades del usuario y las configuraciones del clúster.

¿Qué hace kubectl get storageclass?
Cuando ejecutas el comando kubectl get storageclass, Kubernetes te muestra una lista de las clases de almacenamiento definidas en el clúster, junto con sus propiedades y configuraciones principales. Esto es útil para ver qué tipos de almacenamiento están disponibles y qué parámetros se utilizan para crear los volúmenes persistentes.


- kubectl get pv: obtenemos los persistence volumes. obtienes una lista de los volúmenes persistentes disponibles, mostrando detalles básicos sobre cada volumen, como su nombre, capacidad, estado, acceso y la StorageClass asociada.

- kubectl get pvc: se utiliza para listar los PersistentVolumeClaims (PVCs) en un clúster de Kubernetes. Los PersistentVolumeClaims (PVCs) son solicitudes de almacenamiento realizadas por los usuarios, que definen el tamaño y las características del almacenamiento que necesitan para un pod.

<h3>Storage Options in Kubernetes</h3>

StorageClass: Defines the type and characteristics of storage provided by the cluster. It allows administrators to describe the "classes" of storage they offer. 

PersistentVolume (PV): Represents a piece of storage in the cluster that has been provisioned by an administrator or dynamically using a StorageClass. It's a resource in the cluster that persists beyond pod lifecycles.

PersistentVolumeClaim (PVC): A request for storage by a user. It specifies the amount and characteristics of storage needed by a pod. Once bound to a PV, the PVC can be used by a pod to access the storage.

Manually: We create the Persistent Volume (PV) and the Persistent Volume Claim (PVC)

Dynamically: We create the Persistent Volume Claim (PVC) against the named StorageClass.

This then creates the Persistent Volume (PV) for us



Explicacion a eso: 

Los términos **StorageClass**, **PersistentVolume (PV)** y **PersistentVolumeClaim (PVC)** son fundamentales en Kubernetes para manejar el almacenamiento persistente y dinámico dentro de un clúster. Vamos a desglosarlos con más detalle:

### 1. **StorageClass** (Clase de Almacenamiento)

- **Definición**: La **StorageClass** es un recurso de Kubernetes que define un conjunto de características de almacenamiento que el clúster puede ofrecer. Es una especie de "plantilla" o "clase" que permite a los administradores del clúster describir las capacidades y características del almacenamiento disponible, como el tipo de almacenamiento (por ejemplo, SSD, HDD, almacenamiento en la nube), la política de aprovisionamiento, y otros parámetros específicos de los proveedores de almacenamiento.
  
- **¿Qué hace?**: La StorageClass permite definir diferentes "tipos" de almacenamiento que pueden ser utilizados por los usuarios al crear **PersistentVolumeClaims (PVCs)**. Esto facilita la administración de diferentes clases de almacenamiento (por ejemplo, de alto rendimiento o de bajo costo) en un solo clúster.

- **Ejemplo de StorageClass**:

    ```yaml
    apiVersion: storage.k8s.io/v1
    kind: StorageClass
    metadata:
      name: standard
    provisioner: kubernetes.io/aws-ebs
    parameters:
      type: gp2
    ```

    En este ejemplo, `standard` es una StorageClass que utiliza el provisionador `kubernetes.io/aws-ebs` para crear volúmenes de tipo `gp2` en AWS (Elastic Block Store).

### 2. **PersistentVolume (PV)** (Volumen Persistente)

- **Definición**: Un **PersistentVolume (PV)** es una unidad de almacenamiento dentro del clúster de Kubernetes que ha sido provisionada por un administrador o de manera dinámica utilizando una StorageClass. Representa una pieza de almacenamiento físico o lógico dentro del clúster que persiste más allá del ciclo de vida de un pod.

- **¿Qué hace?**: El PV es la representación del almacenamiento real disponible para los pods. Puede ser una unidad de almacenamiento local, un disco en la nube (como AWS EBS, Google Persistent Disk, Azure Disk), o cualquier otro tipo de almacenamiento respaldado que Kubernetes pueda gestionar. Los administradores del clúster pueden provisionar estos volúmenes manualmente o permitir que se creen dinámicamente a partir de una StorageClass.

- **Ejemplo de PersistentVolume**:

    ```yaml
    apiVersion: v1
    kind: PersistentVolume
    metadata:
      name: pv-example
    spec:
      capacity:
        storage: 5Gi
      volumeMode: Filesystem
      accessModes:
        - ReadWriteOnce
      persistentVolumeReclaimPolicy: Retain
      storageClassName: standard
      csi:
        driver: ebs.csi.aws.com
        volumeHandle: vol-0f5e52a3d9c8ab2b3
    ```

    Este **PersistentVolume** tiene una capacidad de 5Gi, es accesible con el modo `ReadWriteOnce`, y está asociado a la **StorageClass** `standard`. Está provisionado por el controlador CSI de AWS para un volumen de tipo EBS.

### 3. **PersistentVolumeClaim (PVC)** (Reclamación de Volumen Persistente)

- **Definición**: Un **PersistentVolumeClaim (PVC)** es una solicitud de almacenamiento hecha por un usuario o aplicación que ejecuta un pod. Los usuarios crean PVCs para reclamar volúmenes con las características específicas que necesitan, como tamaño, modo de acceso, y almacenamiento de respaldo (por ejemplo, SSD o HDD).

- **¿Qué hace?**: El PVC describe el tipo de almacenamiento que una aplicación necesita. Cuando un PVC se crea, Kubernetes buscará un **PersistentVolume** (PV) que satisfaga esa solicitud (tamaño, características de acceso, etc.). Una vez que se encuentra un PV que coincida con los requisitos del PVC, el PV se vincula al PVC, y el pod puede usar ese volumen para almacenar datos.

- **Ejemplo de PersistentVolumeClaim**:

    ```yaml
    apiVersion: v1
    kind: PersistentVolumeClaim
    metadata:
      name: pvc-example
    spec:
      accessModes:
        - ReadWriteOnce
      resources:
        requests:
          storage: 5Gi
      storageClassName: standard
    ```

    Este **PersistentVolumeClaim** solicita un volumen de 5Gi de almacenamiento con el modo de acceso `ReadWriteOnce`, y utiliza la **StorageClass** `standard`.

### Tipos de Aprovisionamiento de Volúmenes:

Existen dos formas principales de manejar el aprovisionamiento de **PersistentVolumes (PVs)**:

#### 1. **Aprovisionamiento Manual**:

En este enfoque, los administradores de Kubernetes crean los **PersistentVolumes (PVs)** manualmente antes de que los usuarios creen los **PersistentVolumeClaims (PVCs)**. Una vez que el PV está disponible, los usuarios pueden crear un PVC que se vincule con un PV específico.

- **Proceso**:
    - El administrador crea un **PersistentVolume (PV)** manualmente.
    - El usuario crea un **PersistentVolumeClaim (PVC)**.
    - El PVC se vincula con un PV disponible que satisfaga la solicitud.

**Ejemplo**:

- El administrador crea un **PV** con un volumen de 10Gi.
- El usuario crea un **PVC** solicitando 5Gi, que se vincula con el **PV** de 10Gi.

#### 2. **Aprovisionamiento Dinámico**:

En este caso, no es necesario que el administrador cree manualmente un **PersistentVolume (PV)**. Cuando un usuario crea un **PersistentVolumeClaim (PVC)** y especifica una **StorageClass**, Kubernetes puede aprovisionar dinámicamente un **PV** que satisfaga esa solicitud utilizando la StorageClass especificada. Esto es más eficiente porque automatiza el aprovisionamiento del almacenamiento según las necesidades del usuario sin intervención manual.

- **Proceso**:
    - El usuario crea un **PersistentVolumeClaim (PVC)** que especifica una **StorageClass**.
    - Kubernetes, a través del provisionador configurado para esa **StorageClass**, crea automáticamente un **PersistentVolume (PV)** que cumple con las especificaciones del PVC.

**Ejemplo**:

- El usuario crea un **PVC** que solicita 10Gi con una **StorageClass** `fast`.
- Kubernetes aprovisiona automáticamente un **PV** de 10Gi utilizando el proveedor de almacenamiento especificado por la **StorageClass** `fast` (por ejemplo, un volumen SSD de alto rendimiento).

### Resumen:

- **StorageClass**: Define las características del almacenamiento disponible en el clúster (como el tipo de disco, el proveedor de almacenamiento, etc.).
- **PersistentVolume (PV)**: Representa el almacenamiento real en el clúster, que puede ser provisionado manualmente o dinámicamente.
- **PersistentVolumeClaim (PVC)**: Es una solicitud de almacenamiento hecha por un usuario o pod. Una vez que el PVC se vincula a un PV, el pod puede utilizarlo para almacenar datos.

- storageClassName es un campo clave que vincula un PersistentVolume (PV) y un PersistentVolumeClaim (PVC) con una StorageClass específica. Al usar storageClassName en un PV o un PVC, el usuario puede elegir qué tipo de almacenamiento desea, y Kubernetes se encargará de gestionar el volumen de acuerdo con esa especificación.
  


Y dependiendo de si prefieres un enfoque **manual** o **dinámico**, puedes gestionar cómo se aprovisiona el almacenamiento en tu clúster Kubernetes.



El valor DirectoryOrCreate es un tipo específico de volumen en Kubernetes que se utiliza dentro de una configuración de un volumeMount o un volume. Es parte del tipo de volumen emptyDir, que crea un directorio temporal dentro del pod, pero con la peculiaridad de que garantiza que dicho directorio se creará si no existe.

    apiVersion: v1              #Creamos un Volumen (Almacenamiento o Storage Persistente)
    kind: PersistentVolume
    metadata:
      name: manual-pv001
    spec:
      storageClassName: local-path
      capacity:
       storage: 10Gi
      accessModes:
        - ReadWriteOnce
      hostPath:
        path: "/var/lib/rancher/k3s/storage/manual-pv001"
        type: DirectoryOrCreate


Me Ocurrio este error: 

Understanding the Error: Immutable PersistentVolume

The error message you're seeing indicates that you're trying to modify an existing PersistentVolume (PV) in a way that Kubernetes doesn't allow. Specifically, you're attempting to change the Type field of the HostPath volume source, which is immutable after the PV is created.

Why is it Immutable?

Kubernetes enforces immutability on certain fields of a PV to ensure consistency and prevent accidental modifications that could lead to data loss or corruption. Once a PV is created, its underlying storage and configuration are fixed to ensure reliable data operations.

Fue porque le agregamos lo siguiente:

![image](https://github.com/user-attachments/assets/dbd59fed-c814-43e5-8b7f-aae99a0b0272)



<h3>Crear un PersistenceVolumeClaim</h3>

The next step is to create a PersistentVolumeClaim. Pods use PersistentVolumeClaims to request physical storage. In this exercise, you create a PersistentVolumeClaim that requests a volume of at least three gibibytes that can provide read-write access for at most one Node at a time.

    apiVersion: v1
    kind: PersistentVolumeClaim   # Creamos un persistenceVolumeClaim (Persistence Storage)
    metadata:
      name: task-pv-claim
    spec:
      storageClassName: manual
      accessModes:
        - ReadWriteOnce
      resources:
        requests:
          storage: 3Gi




<h3>Claims As Volumes</h3>
Pods access storage by using the claim as a volume. Claims must exist in the same namespace as the Pod using the claim. The cluster finds the claim in the Pod's namespace and uses it to get the PersistentVolume backing the claim. The volume is then mounted to the host and into the Pod.

    apiVersion: v1
    kind: Pod
    metadata:
      name: mypod
    spec:
      containers:
        - name: myfrontend
          image: nginx
          volumeMounts:
          - mountPath: "/var/www/html"
            name: mypd
      volumes:
        - name: mypd
          persistentVolumeClaim:
            claimName: myclaim



Kubernetes Storage - Further Study

Although Rook is a Cloud Native solution on the CNCF Landscape, for the KCNA examination you should also be aware of Ceph, an offering from RedHat that provides object, block and file storage in one solution.

Given the commercial nature of Ceph's relationship with RedHat, it is sometimes used as a storage solution in the OpenShift distribution of Kubernetes. From a KCNA viewpoint you should be aware of the project and it being a unified object/block and file solution.


If this project is of interest, see the following resources -

https://www.redhat.com/en/technologies/storage/ceph

https://docs.openshift.com/container-platform/3.11/install_config/storage_examples/ceph_example.html



<h2>Questions</h2>

What is the primary characteristic of ephemeral storage in Kubernetes?
- It is used for long-term data storage
- It persists across restarts
- It does not survive across restarts (Correct)
- It is mainly used for database storage


In the context of Kubernetes, what is an example of ephemeral storage?
- PersistentVolume
- emptyDir (correct)
- HostPath
- NFS

What is the primary purpose of a Persistent Volume (PV) in Kubernetes?
- To provide temporary storage for pods
- To automatically delete data when a pod is deleted
- To store data that persists beyond the lifecycle of a pod (Correct)
- To enhance the performance of ephemeral storage



What does the Reclaim Policy 'Retain' imply in Kubernetes storage?
- The storage is deleted immediately after the pod is deleted
- The storage is recycled for future use
- The data is kept until the volume is manually deleted (Correct)
- The storage is available for dynamic provisioning


Explanation: 

En Kubernetes, la Política de Recuperación (Reclaim Policy) de un PersistentVolume (PV) determina qué sucede con el volumen una vez que se libera (cuando se elimina el PersistentVolumeClaim (PVC) que estaba vinculado a él).

La Política de Recuperación Retain significa que los datos se mantienen hasta que el volumen sea eliminado manualmente. Esta política asegura que el volumen no se elimine automáticamente cuando se elimina el PVC. En su lugar, permanece en estado Released (Liberado) y los datos se mantienen intactos, lo que permite a los administradores gestionar manualmente el ciclo de vida del volumen (incluyendo la recuperación de datos, respaldos o eliminación manual).



How is a PersistentVolumeClaim (PVC) in Kubernetes typically used?
- To allocate ephemeral storage to pods
- To delete storage volumes automatically
- To claim storage resources defined by a PersistentVolume (correct)
- To increase the storage capacity dynamically


Explanation:

En Kubernetes, un PersistentVolumeClaim (PVC) se usa para solicitar y reclamar recursos de PersistentVolume (PV). Un PVC especifica el tamaño, el modo de acceso (por ejemplo, ReadWriteOnce, ReadOnlyMany) y, opcionalmente, una StorageClass para el tipo de almacenamiento requerido. El PVC actúa como una solicitud de almacenamiento, y Kubernetes hará lo siguiente:

1. Vinculará el PVC a un PersistentVolume (PV) existente que coincida con su solicitud (tamaño, modo de acceso y, opcionalmente, la StorageClass).
2. Si no existe un PV adecuado, Kubernetes puede aprovisionar dinámicamente un nuevo PersistentVolume (si el aprovisionamiento dinámico está configurado).

   
Esto permite a los usuarios separar la solicitud de almacenamiento (PVC) del almacenamiento físico subyacente (PV), lo que facilita la gestión del almacenamiento en un entorno nativo de la nube.


In Kubernetes, what is the significance of setting a volume's emptyDir.medium to Memory?
- It specifies the volume is used for database storage
- It configures the volume as a high-performance cache area (correct)
- It designates the volume for long-term data storage
- It makes the volume available for dynamic provisioning


Explanation:

En Kubernetes, el volumen de tipo emptyDir se crea cuando un pod se inicia y se elimina cuando el pod termina. Por defecto, un volumen emptyDir se almacena en el sistema de archivos del nodo. Sin embargo, si se establece el campo medium de emptyDir como Memory, el volumen se almacena en la memoria RAM del nodo en lugar de en el disco.

Esto tiene implicaciones importantes:

Almacenamiento en memoria: El volumen se convierte en un almacenamiento de alto rendimiento, ya que la memoria RAM es mucho más rápida que el almacenamiento en disco. Es ideal para usarlo como un área de caché de alto rendimiento, donde se necesitan accesos rápidos y temporales a los datos.
Volumen efímero: Este tipo de volumen es efímero, lo que significa que los datos se perderán cuando el pod se elimine o se reinicie.



What happens to a Kubernetes PersistentVolume with a Reclaim Policy of 'Delete' after its associated PVC is deleted?
- The volume is retained for future use
- The volume is automatically recycled
- The underlying storage is deleted along with the volume (correct)
- The volume is converted to ephemeral storage


Explanation:

When a PersistentVolume (PV) has a Reclaim Policy set to Delete, it means that the underlying storage associated with the PV (such as a cloud disk, file system, or other physical storage) will be deleted automatically when the PersistentVolumeClaim (PVC) bound to it is deleted.

This is useful in scenarios where the storage is not needed after the PVC is no longer in use (for example, in cloud environments, where volumes can be provisioned and managed dynamically). The deletion of the PVC triggers the cleanup of both the Kubernetes PV and the underlying storage resource, which is removed by Kubernetes to avoid leaving orphaned resources.

Cuando un PersistentVolume (PV) tiene una Política de Recuperación (Reclaim Policy) configurada como Delete, significa que el almacenamiento subyacente asociado con el PV (como un disco en la nube, un sistema de archivos, o cualquier otro recurso de almacenamiento físico) se elimina automáticamente cuando se elimina el PersistentVolumeClaim (PVC) vinculado a él.
Esto es útil en escenarios donde el almacenamiento ya no es necesario después de que el PVC ha dejado de usarse (por ejemplo, en entornos de nube, donde los volúmenes pueden ser aprovisionados y gestionados de manera dinámica). La eliminación del PVC desencadena la limpieza tanto del PV en Kubernetes como del recurso de almacenamiento subyacente, que se elimina para evitar dejar recursos huérfanos.



In the video example what was the purpose of adding a nodeSelector to the pod configuration?
- To schedule the pod on a node with the highest available resources
- To ensure the pod runs on a specific node due to storage limitations (correct)
- To improve the performance of the pod
- To allocate dynamic storage to the pod


How is dynamic provisioning of storage in Kubernetes different from manual provisioning?
- Dynamic provisioning does not use PersistentVolumes
- In dynamic provisioning, volumes are created automatically when a PVC is made (correct)
- Dynamic provisioning is used only for ephemeral storage 
- Manual provisioning is faster and more efficient than dynamic provisioning


Explanation

Dynamic provisioning in Kubernetes refers to the automatic creation of PersistentVolumes (PVs) when a PersistentVolumeClaim (PVC) is made. With dynamic provisioning, there is no need for the administrator to manually create the PV ahead of time. Instead, when a PVC is created, Kubernetes will automatically provision a PV based on the specifications of the PVC and the associated StorageClass.



Which storage solution is known for providing comprehensive storage capabilities, including block, file, and object storage, in distributed systems?
- NFS
- GlusterFS
- Ceph (correct)
- iSCSI

Explanation: 

Ceph is a highly scalable, distributed storage system that provides unified storage capabilities, including block, file, and object storage. It is designed to handle large amounts of data in a fault-tolerant and scalable manner, making it ideal for distributed systems. Ceph's architecture allows it to scale horizontally by adding more nodes and offers a single platform for different types of storage workloads.



Importante conocer sobre Ceph

Ceph (pronounced /ˈsɛf/) is a free and open-source software-defined storage platform that provides object storage,[7] block storage, and file storage built on a common distributed cluster foundation. Ceph provides distributed operation without a single point of failure and scalability to the exabyte level. Since version 12 (Luminous), Ceph does not rely on any other conventional filesystem and directly manages HDDs and SSDs with its own storage backend BlueStore and can expose a POSIX filesystem.

Ceph replicates data with fault tolerance,[8] using commodity hardware and Ethernet IP and requiring no specific hardware support. Ceph is highly available and ensures strong data durability through techniques including replication, erasure coding, snapshots and clones. By design, the system is both self-healing and self-managing, minimizing administration time and other costs.


<h2>StatefulSets</h2>

Kubernetes StatefulSets - Study Tips
For the KCNA examination, please focus on the following areas -

The purpose of StatefulSets
The difference/similarities between StatefulSets and Deployments
The StatefulSet relation/dependency on Services for naming


Definicion - k8s web sites

![image](https://github.com/user-attachments/assets/a76e7d52-ed3b-49ac-9745-97e75f5660b5)


Gestiona el despliegue y escalado de un conjunto de Pods, y garantiza el orden y unicidad de dichos Pods.

Al igual que un Deployment, un StatefulSet gestiona Pods que se basan en una especificación idéntica de contenedor. A diferencia de un Deployment, un StatefulSet mantiene una identidad asociada a sus Pods. Estos pods se crean a partir de la misma especificación, pero no pueden intercambiarse; cada uno tiene su propio identificador persistente que mantiene a lo largo de cualquier re-programación.

Un StatefulSet opera bajo el mismo patrón que cualquier otro controlador. Se define el estado deseado en un objeto StatefulSet, y el controlador del StatefulSet efectúa las actualizaciones que sean necesarias para alcanzarlo a partir del estado actual.

Usar StatefulSets
Los StatefulSets son valiosos para aquellas aplicaciones que necesitan uno o más de los siguientes:

Identificadores de red estables, únicos.
Almacenamiento estable, persistente.
Despliegue y escalado ordenado, controlado.
Actualizaciones en línea ordenadas, automatizadas.
De los de arriba, estable es sinónimo de persistencia entre (re)programaciones de Pods. Si una aplicación no necesita ningún identificador estable o despliegue, eliminación, o escalado ordenado, deberías desplegar tu aplicación con un controlador que proporcione un conjunto de réplicas sin estado, como un Deployment o un ReplicaSet, ya que están mejor preparados para tus necesidades sin estado.

Limitaciones
El almacenamiento de un determinado Pod debe provisionarse por un Provisionador de PersistentVolume basado en la storage class requerida, o pre-provisionarse por un administrador.
Eliminar y/o reducir un StatefulSet no eliminará los volúmenes asociados con el StatefulSet. Este comportamiento es intencional y sirve para garantizar la seguridad de los datos, que da más valor que la purga automática de los recursos relacionados del StatefulSet.
Los StatefulSets actualmente necesitan un Servicio Headless como responsable de la identidad de red de los Pods. Es tu responsabilidad crear este Service.
Los StatefulSets no proporcionan ninguna garantía de la terminación de los pods cuando se elimina un StatefulSet. Para conseguir un término de los pods ordenado y controlado en el StatefulSet, es posible reducir el StatefulSet a 0 réplicas justo antes de eliminarlo.
Cuando se usan las Actualizaciones en línea con la Regla de Gestión de Pod (OrderedReady) por defecto, es posible entrar en un estado inconsistente que requiere de una intervención manual para su reparación.
Componentes
El ejemplo de abajo demuestra los componentes de un StatefulSet:

Un servicio Headless, llamado nginx, se usa para controlar el dominio de red.
Un StatefulSet, llamado web, que tiene una especificación que indica que se lanzarán 3 réplicas del contenedor nginx en Pods únicos.
Un volumeClaimTemplate que proporciona almacenamiento estable por medio de PersistentVolumes provisionados por un provisionador de tipo PersistentVolume.
             apiVersion: v1
             kind: Service
             metadata:
               name: nginx
               labels:
                 app: nginx
             spec:
               ports:
               - port: 80
                 name: web
               clusterIP: None
               selector:
                 app: nginx
             ---
             apiVersion: apps/v1
             kind: StatefulSet
             metadata:
               name: web
             spec:
               selector:
                 matchLabels:
                   app: nginx # tiene que coincidir con .spec.template.metadata.labels
               serviceName: "nginx"
               replicas: 3 # por defecto es 1
               template:
                 metadata:
                   labels:
                     app: nginx # tiene que coincidir con .spec.selector.matchLabels
                 spec:
                   terminationGracePeriodSeconds: 10
                   containers:
                   - name: nginx
                     image: registry.k8s.io/nginx-slim:0.8
                     ports:
                     - containerPort: 80
                       name: web
                     volumeMounts:
                     - name: www
                       mountPath: /usr/share/nginx/html
               volumeClaimTemplates:
               - metadata:
                   name: www
                 spec:
                   accessModes: [ "ReadWriteOnce" ]
                   storageClassName: "my-storage-class"
                   resources:
                     requests:
                       storage: 1Gi
    
Selector de Pod
Debes poner el valor del campo .spec.selector de un StatefulSet para que coincida con las etiquetas de su campo .spec.template.metadata.labels. Antes de Kubernetes 1.8, el campo .spec.selector se predeterminaba cuando se omitía. A partir de la versión 1.8, si no se especifica un selector de coincidencia de Pods, se produce un error de validación durante la creación del StatefulSet.

Identidad de Pod
Los Pods de un StatefulSet tienen una identidad única que está formada por un ordinal, una identidad estable de red, y almacenamiento estable. La identidad se asocia al Pod, independientemente del nodo en que haya sido (re)programado.

Índice Ordinal
Para un StatefulSet con N réplicas, a cada Pod del StatefulSet se le asignará un número entero ordinal, desde 0 hasta N-1, y que es único para el conjunto.

ID estable de Red
El nombre de anfitrión (hostname) de cada Pod de un StatefulSet se deriva del nombre del StatefulSet y del número ordinal del Pod. El patrón para construir dicho hostname es $(statefulset name)-$(ordinal). Así, el ejemplo de arriba creará tres Pods denominados web-0,web-1,web-2. Un StatefulSet puede usar un Servicio Headless para controlar el nombre de dominio de sus Pods. El nombre de dominio gestionado por este Service tiene la forma: $(service name).$(namespace).svc.cluster.local, donde "cluster.local" es el nombre de dominio del clúster. Conforme se crea cada Pod, se le asigna un nombre DNS correspondiente de subdominio, que tiene la forma: $(podname).$(governing service domain), donde el servicio en funciones se define por el campo serviceName del StatefulSet.

Como se indicó en la sección limitaciones, la creación del Servicio Headless encargado de la identidad de red de los pods es enteramente tu responsabilidad.

Aquí se muestran algunos ejemplos de elecciones de nombres de Cluster Domain, nombres de Service, nombres de StatefulSet, y cómo impactan en los nombres DNS de los Pods del StatefulSet:

Cluster Domain	Service (ns/nombre)	StatefulSet (ns/nombre)	StatefulSet Domain	Pod DNS	Pod Hostname
cluster.local	default/nginx	default/web	nginx.default.svc.cluster.local	web-{0..N-1}.nginx.default.svc.cluster.local	web-{0..N-1}
cluster.local	foo/nginx	foo/web	nginx.foo.svc.cluster.local	web-{0..N-1}.nginx.foo.svc.cluster.local	web-{0..N-1}
kube.local	foo/nginx	foo/web	nginx.foo.svc.kube.local	web-{0..N-1}.nginx.foo.svc.kube.local	web-{0..N-1}
Nota:
El valor de Cluster Domain se pondrá a cluster.local a menos que se configure de otra forma.
Almacenamiento estable
Kubernetes crea un PersistentVolume para cada VolumeClaimTemplate. En el ejemplo de nginx de arriba, cada Pod recibirá un único PersistentVolume con una StorageClass igual a my-storage-class y 1 GiB de almacenamiento provisionado. Si no se indica ninguna StorageClass, entonces se usa la StorageClass por defecto. Cuando un Pod se (re)programa en un nodo, sus volumeMounts montan los PersistentVolumes asociados con sus PersistentVolume Claims. Nótese que los PersistentVolumes asociados con los PersistentVolume Claims de los Pods no se eliminan cuando los Pods, o los StatefulSet se eliminan. Esto debe realizarse manualmente.

Etiqueta de Nombre de Pod
Cuando el controlador del StatefulSet crea un Pod, añade una etiqueta, statefulset.kubernetes.io/pod-name, que toma el valor del nombre del Pod. Esta etiqueta te permite enlazar un Service a un Pod específico en el StatefulSet.

Garantías de Despliegue y Escalado
Para un StatefulSet con N réplicas, cuando los Pods se despliegan, se crean secuencialmente, en orden de {0..N-1}.
Cuando se eliminan los Pods, se terminan en orden opuesto, de {N-1..0}.
Antes de que una operación de escalado se aplique a un Pod, todos sus predecesores deben estar Running y Ready.
Antes de que se termine un Pod, todos sus sucesores deben haberse apagado completamente.
El StatefulSet no debería tener que indicar un valor 0 para el campo pod.Spec.TerminationGracePeriodSeconds. Esta práctica no es segura y se aconseja no hacerlo. Para una explicación más detallada, por favor echa un vistazo a cómo forzar la eliminación de Pods de un StatefulSet.

Cuando el ejemplo nginx de arriba se crea, se despliegan tres Pods en el orden web-0, web-1, web-2. web-1 no se desplegará hasta que web-0 no esté Running y Ready, y web-2 no se desplegará hasta que web-1 esté Running y Ready. En caso de que web-0 fallase, después de que web-1 estuviera Running y Ready, pero antes de que se desplegara web-2, web-2 no se desplegaría hasta que web-0 se redesplegase con éxito y estuviera Running y Ready.

Si un usuario fuera a escalar el ejemplo desplegado parcheando el StatefulSet de forma que replicas=1, web-2 se terminaría primero. web-1 no se terminaría hasta que web-2 no se hubiera apagado y eliminado por completo. Si web-0 fallase después de que web-2 se hubiera terminado y apagado completamente, pero antes del término de web-1, entonces web-1 no se terminaría hasta que web-0 estuviera Running y Ready.

Reglas de Gestión de Pods
En Kubernetes 1.7 y versiones posteriores, el StatefulSet permite flexibilizar sus garantías de ordenación al mismo tiempo que preservar su garantía de singularidad e identidad a través del campo .spec.podManagementPolicy.

Gestión de tipo OrderedReady de Pods
La gestión de tipo OrderedReady de pods es la predeterminada para los StatefulSets. Implementa el comportamiento descrito arriba.

Gestión de tipo Parallel de Pods
La gestión de tipo Parallel de pods le dice al controlador del StatefulSet que lance y termine todos los Pods en paralelo, y que no espere a que los Pods estén Running y Ready o completamente terminados antes de lanzar o terminar otro Pod.

Estrategias de Actualización
En Kubernetes 1.7 y a posteriori, el campo .spec.updateStrategy del StatefulSet permite configurar y deshabilitar las actualizaciones automátizadas en línea para los contenedores, etiquetas, peticiones/límites de recursos, y anotaciones de los Pods del StatefulSet.

On Delete
La estrategia de actualización OnDelete implementa el funcionamiento tradicional (1.6 y previo). Cuando el campo .spec.updateStrategy.type de un StatefulSet se pone al valor OnDelete, el controlador del StatefulSet no actualizará automáticamente los Pods del StatefulSet. Los usuarios deben eliminar manualmente los Pods para forzar al controlador a crear nuevos Pods que reflejen las modificaciones hechas al campo .spec.template del StatefulSet.

Rolling Updates
La estrategia de actualización RollingUpdate implementa una actualización automatizada en línea de los Pods del StatefulSet. Es la estrategia por defecto cuando el campo .spec.updateStrategy se deja sin valor. Cuando el campo .spec.updateStrategy.type de un StatefulSet se pone al valor RollingUpdate, el controlador del StatefulSet lo eliminará y recreará cada Pod en el StatefulSet. Procederá en el mismo orden en que ha terminado los Pod (del número ordinal más grande al más pequeño), actualizando cada Pod uno por uno. Esperará a que el Pod actualizado esté Running y Ready antes de actualizar su predecesor.

Particiones
La estrategia de actualización RollingUpdate puede particionarse, indicando el valor del campo .spec.updateStrategy.rollingUpdate.partition. Si se indica una partición, todos los Pods con un número ordinal mayor o igual que el de la partición serán actualizados cuando el campo .spec.template del StatefulSet se actualice. Todos los Pods con un número ordinal que sea menor que el de la partición no serán actualizados, e incluso si son eliminados, serán recreados con la versión anterior. Si el campo .spec.updateStrategy.rollingUpdate.partition de un StatefulSet es mayor que el valor del campo .spec.replicas, las modificaciones al campo .spec.template no se propagarán a sus Pods. En la mayoría de ocasiones, no necesitarás usar una partición, pero pueden resultar útiles si quieres preparar una actualización, realizar un despliegue tipo canary, o llevar a cabo un despliegue en fases.



En Kubernetes, un StatefulSet es un controlador que garantiza que un número estable de réplicas pod identicos estén en ejecución en todo momento. A diferencia de los Deployments, los StatefulSets mantienen una identidad estable para cada pod, lo que los hace ideales para aplicaciones que requieren:

Identidad estable: Cada pod tiene un nombre único y una IP estática, lo que es crucial para servicios de estado como bases de datos o sistemas de almacenamiento distribuidos.
Orden de escalado: Los pods se crean y se eliminan de forma ordenada, lo que es importante para las aplicaciones que dependen de un estado persistente.
Volumen persistente: Los StatefulSets pueden ser configurados para usar volúmenes persistentes, lo que garantiza que los datos de la aplicación no se pierdan si un pod se reinicia o se reemplaza.
Aplicaciones típicas de StatefulSets:

Bases de datos: Bases de datos relacionales como MySQL o PostgreSQL, donde cada pod representa una instancia de la base de datos.
Sistemas de almacenamiento distribuidos: Sistemas de archivos distribuidos como Ceph o GlusterFS, donde cada pod es un nodo en el clúster.
Servicios de estado: Cualquier aplicación que requiera mantener un estado persistente entre reinicios, como servicios de caché o colas de mensajes.
Características clave de StatefulSets:

Escalado: Puedes escalar un StatefulSet hacia arriba o hacia abajo para aumentar o disminuir el número de réplicas.
Actualización: Kubernetes puede actualizar automáticamente los pods de un StatefulSet sin perder datos.
Auto-escalado: Puedes configurar un StatefulSet para escalar automáticamente en función de la carga.
Seleccionador: Los StatefulSets utilizan un selector para identificar los pods que pertenecen al conjunto.
Ventajas de usar StatefulSets:

Facilidad de gestión: Kubernetes se encarga de la creación, escalado y actualización de los pods.
Alta disponibilidad: Los StatefulSets garantizan que siempre haya un número estable de réplicas en ejecución.
Escalabilidad: Puedes escalar tus aplicaciones de forma horizontal para manejar cargas más grandes.
En resumen:

Los StatefulSets son una herramienta poderosa en Kubernetes para gestionar aplicaciones de estado. Si necesitas una aplicación que requiera una identidad estable, un orden de escalado específico y volúmenes persistentes, un StatefulSet es la mejor opción.



<h3>Kubernetes Deployments vs StatefulSets</h3>


StatefulSet
Use 'StatefulSet' with Stateful Distributed Applications, that require each node to have a persistent state. StatefulSet provides the ability to configure an arbitrary number of nodes, for a stateful application/component, through a configuration (replicas = N).

There are two kinds of stateful distributed applications: Master-Master and Master-Slave. All nodes in a Master-Master configuration and Slave nodes in a Master-Slave configuration can make use of a StatefulSet.
Examples:
Master-Slave -> Datanodes (slaves) in a Hadoop cluster
Master-Master -> Database nodes (master-master) in a Cassandra cluster

Each Pod (replica/node) in a StatefulSet has a Unique and Stable network identity. For example in a Cassandra StatefulSet with name as 'cassandra' and number of replica nodes as N, each Cassandra pod (node) has:

Ordinal Index for each pod: 0,1,..,N-1
Stable network id: cassandra-0, cassandra-1,.., cassandra-N-1
A separate persistent volume for each pod against a volume claim template i.e a separate storage for every pod (node)
Pods are created in the order 0 to N-1 and terminated in the reverse order N-1 to 0
Refer: https://kubernetes.io/docs/concepts/workloads/controllers/statefulset/

Deployment
'Deployment' on the other hand is suitable for stateless applications/services where the nodes do not require any special identity. A load balancer can reach any node that it chooses. All nodes are equal. A Deployment is useful for creating any number of arbitrary nodes, through a configuration (replicas = N).


<table border="1">
  <thead>
    <tr>
      <th>Feature</th>
      <th>StatefulSets</th>
      <th>Deployment</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>State</td>
      <td>Statefull</td>
      <td>Stateless</td>
    </tr>
    <tr>
      <td>Definition</td>
      <td>Stateful app: Stateful applications typically involve some database, such as Cassandra, MongoDB, MessageQueue like Kafka, RabbitMQ or MySQL, and processes a read and/or write to it.</td>
      <td>Usually, frontend components have completely different scaling requirements than the backends, so we tend to scale them individually. Not to mention the fact that backends such as databases are usually much harder to scale compared to (stateless) frontend web servers. Yes, the term “stateless” means that no past data nor state is stored or needs to be persistent when a new container is created.</td>
    </tr>
    <tr>
      <td>Behaviour</td>
      <td>When a stateful pod instance dies (or the node it’s running on fails), the pod instance needs to be resurrected on another node, new instance get the same name, network identity, and state as the one it’s replacing.</td>
      <td>Pod replicas managed by a Deployment; they’re mostly stateless, they can be replaced with a completely new pod replica at any time.</td>
    </tr>
    <tr>
      <td>Pod Mechanism</td>
      <td>Pods created by the StatefulSet aren’t exact replicas of each other. Each can have its own set of volumes—in other words, storage (and thus persistent state)—which differentiates it from its peers.</td>
      <td>When a Deployment replaces a pod, the new pod is a completely new pod with a new hostname and IP.</td>
    </tr>
  </tbody>
</table>



![image](https://github.com/user-attachments/assets/d9f9fad0-4e16-41fe-9cbb-5666ddca68bc)

Statefulsets are valuable for applications that require one or more of the following:

1. Stable Unique Network Identifiers
2. Stable Persistent Storage
3. Ordered Graceful Deployment and Scaling
4. Ordered Automated Rolling Updates

Commands

kubectl get statefulset: obtenemos los statefullstes



Ejemplo de statefullset en el curso de Spurin:

    apiVersion: apps/v1
    kind: StatefulSet
    metadata:
      labels:
        app: nginx
      name: my-server-nginx
    spec:
      replicas: 3
      selector:
        matchLabels:
          app: nginx
      serviceName: nginx
      template:
        metadata:
          creationTimestamp: null
          labels:
            app: nginx
        spec:
          containers:
          - image: nginx
            name: nginx
             
No los crea ordenado: 

![image](https://github.com/user-attachments/assets/77fa2268-a413-456d-b721-1318addebfde)


![image](https://github.com/user-attachments/assets/c4e9259d-dd2b-4803-a656-10e655c49d50)


![image](https://github.com/user-attachments/assets/1fee7784-f78c-4fed-bb0e-fde826db0473)


Vamos a evaluar las caracteristicas de un statefulset:

![image](https://github.com/user-attachments/assets/55019f38-72e6-42f3-be55-41ba72b9a336)

Binding de las replicas con un servicio de tipo ClusterIp que creo Spurin

![image](https://github.com/user-attachments/assets/d2430bbd-e8ab-4d14-914d-b797db094db6)




Le agregamos la propiedad volumeClaimtemplates

![image](https://github.com/user-attachments/assets/db1c0769-96a1-4e92-b42f-5efced8109d7)



n Kubernetes, un VolumeClaimTemplate es un recurso utilizado dentro de los objetos StatefulSet para gestionar volúmenes persistentes de manera dinámica y repetitiva. En términos sencillos, permite que cada pod dentro de un StatefulSet tenga un volumen persistente dedicado, con el mismo nombre y propiedades, sin necesidad de configurarlo manualmente.

Explicación detallada:
Contexto:

En Kubernetes, un PersistentVolumeClaim (PVC) es un objeto que solicita almacenamiento persistente en un clúster, sin especificar un volumen concreto, lo que permite que Kubernetes gestione el almacenamiento de forma dinámica.
Un StatefulSet se utiliza para aplicaciones con estado, donde cada pod necesita una identidad persistente y un almacenamiento persistente único.
Uso de volumeClaimTemplates:

En un StatefulSet, puedes definir un volumeClaimTemplate, que es una plantilla para crear PVCs para cada pod del StatefulSet.
Kubernetes crea automáticamente un PVC único para cada pod, de acuerdo con las especificaciones definidas en la plantilla. Esto garantiza que cada pod tenga su propio volumen persistente que se crea cuando el pod es programado en un nodo.
Propósito:

El principal propósito de un volumeClaimTemplate es proporcionar almacenamiento persistente de forma dinámica para cada pod del StatefulSet, asegurando que cada uno de estos pods tenga su propio volumen de almacenamiento con las características definidas en la plantilla.
Ejemplo:
Aquí tienes un ejemplo básico de un StatefulSet que utiliza volumeClaimTemplates para crear volúmenes persistentes para cada pod:


          apiVersion: apps/v1
          kind: StatefulSet
          metadata:
            name: my-stateful-app
          spec:
            serviceName: "my-service"
            replicas: 3
            selector:
              matchLabels:
                app: my-stateful-app
            template:
              metadata:
                labels:
                  app: my-stateful-app
              spec:
                containers:
                  - name: my-container
                    image: my-image
                    volumeMounts:
                      - name: my-storage
                        mountPath: /data
            volumeClaimTemplates:
              - metadata:
                  name: my-storage
                spec:
                  accessModes:
                    - ReadWriteOnce
                  resources:
                    requests:
                      storage: 1Gi
                  storageClassName: standard
Descripción del ejemplo:
volumeClaimTemplates: En este bloque definimos la plantilla para crear los PersistentVolumeClaims para cada pod en el StatefulSet. En este caso, se crea un volumen con el nombre my-storage.
spec dentro de volumeClaimTemplates: Define las características del PVC, como el tamaño (1Gi), el acceso (ReadWriteOnce), y la clase de almacenamiento (standard).
¿Qué sucede cuando se crea el StatefulSet?
Kubernetes creará automáticamente tres PVCs para los tres pods del StatefulSet con los nombres my-storage-0, my-storage-1, y my-storage-2.
Cada uno de esos PVCs se monta en el directorio /data dentro de los contenedores de cada pod, proporcionando almacenamiento persistente que se mantiene incluso si el pod se reinicia o se mueve a otro nodo.




Podriamos crear persistenceVolumes
![image](https://github.com/user-attachments/assets/76df2ee4-8396-4c02-a09e-8fa7004de58c)

Flujo general de creación de un volumen persistente con StatefulSet:
StatefulSet con volumeClaimTemplates: Definir un StatefulSet que incluya plantillas de PersistentVolumeClaim (PVC).
Clase de almacenamiento (StorageClass): Configurar una StorageClass que administre la provisión dinámica de los volúmenes.
Provisión de PersistentVolume: Cuando se crea un PVC, si no existe un PersistentVolume (PV) correspondiente, Kubernetes utiliza la StorageClass definida para crear dinámicamente un PV.
Ejemplo práctico:
A continuación, te proporcionaré un ejemplo de cómo crear un StatefulSet que gestione volúmenes persistentes con volumeClaimTemplates.

1. Crear un StorageClass
El primer paso es asegurarte de que tienes una StorageClass configurada en tu clúster de Kubernetes. La StorageClass es la que determina cómo se gestionan y provisionan los volúmenes (por ejemplo, a través de discos locales, NFS, EBS en AWS, etc.).

Ejemplo de un StorageClass básico que usa la provisión dinámica de volúmenes en Kubernetes:

yaml
Copiar código
apiVersion: storage.k8s.io/v1
kind: StorageClass
metadata:
  name: standard
provisioner: kubernetes.io/aws-ebs  # Si usas AWS EBS
parameters:
  type: gp2  # Tipo de disco (si usas AWS EBS)
Este StorageClass le dice a Kubernetes que cree volúmenes persistentes utilizando el proveedor de almacenamiento aws-ebs, que en este caso es un disco de tipo gp2.

2. Crear un StatefulSet con volumeClaimTemplates
Ahora, creamos el StatefulSet, en el cual cada pod dentro del StatefulSet recibirá su propio PVC que estará ligado a un volumen persistente, todo gestionado automáticamente por Kubernetes.


         apiVersion: apps/v1
         kind: StatefulSet
         metadata:
           name: my-stateful-app
         spec:
           serviceName: "my-service"
           replicas: 3
           selector:
             matchLabels:
               app: my-stateful-app
           template:
             metadata:
               labels:
                 app: my-stateful-app
             spec:
               containers:
                 - name: my-container
                   image: my-image
                   volumeMounts:
                     - name: my-storage
                       mountPath: /data
           volumeClaimTemplates:
             - metadata:
                 name: my-storage  # El nombre del PVC será my-storage-0, my-storage-1, etc.
               spec:
                 accessModes:
                   - ReadWriteOnce
                 resources:
                   requests:
                     storage: 1Gi
                 storageClassName: standard  # Aquí asignamos el StorageClass
Explicación:
volumeClaimTemplates: Este bloque dentro del StatefulSet define una plantilla de PersistentVolumeClaim que se usará para cada pod dentro del StatefulSet. Cada pod tendrá su propio PVC, que será nombrado automáticamente como my-storage-0, my-storage-1, etc., y cada uno estará asociado con un volumen persistente único.

storageClassName: standard: Aquí asignamos el StorageClass previamente definido (standard en este caso). Esto le indica a Kubernetes que debe utilizar la provisión dinámica de volúmenes que proporciona el StorageClass, y que los volúmenes deberán ser gestionados por el proveedor de almacenamiento que especifique la clase (por ejemplo, EBS en AWS, o discos locales si usas otros proveedores).

resources.requests.storage: 1Gi: Esto indica que cada PVC debe solicitar 1Gi de almacenamiento. Kubernetes se encargará de asignar el tamaño y tipo de disco según las configuraciones del StorageClass.

¿Qué pasa cuando se crea este StatefulSet?
Cuando se crea el StatefulSet, Kubernetes crea automáticamente un PVC para cada pod. Si no hay un volumen persistente (PV) disponible que coincida con las solicitudes de PVC, Kubernetes provisionará dinámicamente un PV utilizando la StorageClass proporcionada en la plantilla (en este caso, el StorageClass standard).

Si el StatefulSet tiene 3 réplicas, se crearán 3 PVCs (por ejemplo, my-storage-0, my-storage-1, y my-storage-2), y Kubernetes asignará un volumen para cada PVC de acuerdo con la StorageClass definida.

3. Ver los volúmenes persistentes (PV) creados
Una vez que el StatefulSet esté en ejecución, puedes comprobar los PersistentVolumes que han sido creados dinámicamente con el siguiente comando:

bash
Copiar código
kubectl get pv
Deberías ver que Kubernetes ha creado un volumen persistente para cada PVC, y que estos están siendo utilizados por los pods del StatefulSet.



Questions

What is the primary difference between Deployments and StatefulSets in Kubernetes?
- StatefulSets provide a sticky identity for each pod (Correct)
- Deployments are used for stateful applications
- StatefulSets do not support rolling updates
- Deployments manage stateful applications


When a StatefulSet is used in Kubernetes, how does each pod manage its storage?
- Each pod shares a single Persistent Volume
- Each pod creates its own Persistent Volume Claim (Correct)
- All pods use ephemeral storage
- Storage is not supported in StatefulSets


What is the purpose of the 'serviceName' in a StatefulSet's configuration?
- It specifies the name of the service to expose the StatefulSet
- It is used to define a headless service for network identity (Correct)
- It defines the name of the StatefulSet
- It determines the storage class for persistent storage


Explanation:

In a StatefulSet, the serviceName field is used to specify the name of the headless service that will be created for the StatefulSet. This service is responsible for providing network identity to the individual pods within the StatefulSet.

When a StatefulSet is created, Kubernetes automatically creates DNS records for each pod in the StatefulSet based on this serviceName. These DNS records allow direct communication between the pods, ensuring that each pod has a stable, unique network identity that is consistent across pod restarts.

For example, if you set serviceName: "my-headless-service" in the StatefulSet, Kubernetes will create DNS entries like:

my-stateful-app-0.my-headless-service.<namespace>.svc.cluster.local
my-stateful-app-1.my-headless-service.<namespace>.svc.cluster.local
These entries allow other pods or services to access specific pods within the StatefulSet directly.


What happens to the data volume if a pod in a StatefulSet is deleted and recreated?
- The data is lost
- The data persists and is reattached to the new pod  (Correct)
- The data is replicated to other pods
- The data is moved to a backup pod


Explanation:
In Kubernetes, when you use a StatefulSet, each pod typically has its own PersistentVolumeClaim (PVC), which is tied to a PersistentVolume (PV) that stores the pod's data. This setup ensures that even if a pod is deleted and recreated (such as during a restart or scaling operation), its associated data volume remains intact and is reattached to the new pod.

Here’s what happens in more detail:

Pod Deletion: When a pod in a StatefulSet is deleted, the associated PVC (PersistentVolumeClaim) remains intact. The PVC references a PersistentVolume (PV) that holds the pod's data.

Pod Recreation: The StatefulSet ensures that when the pod is recreated (with the same name as before), it is assigned the same PVC. Kubernetes will then reattach the same PersistentVolume (PV) to the new pod, ensuring that the pod has access to its previous data.

This behavior is key to maintaining data persistence in stateful applications, like databases, that need to retain their state even when pods are restarted or rescheduled across nodes.



What is a key benefit of using StatefulSets for stateful applications in Kubernetes?
- They support automatic scaling
- They provide stable network IDs for each pod (Correct)
- They automatically backup data
- They require less configuration than Deployments



Explanation:
One of the key benefits of using StatefulSets in Kubernetes is that they provide stable network identities and stable persistent storage for stateful applications. Here's how this works:

Stable Network IDs: Each pod in a StatefulSet gets a unique, stable network identity. The pods are named sequentially (e.g., pod-0, pod-1, pod-2, etc.), and these names are stable across pod restarts. This enables applications to know exactly which pod they are communicating with, which is essential for many stateful applications, such as databases, where individual pods might need to be addressed directly.

Stable Persistent Storage: Each pod in a StatefulSet also has its own associated PersistentVolumeClaim (PVC), which ensures that the storage is persistent and is not lost when pods are deleted or rescheduled. The PVCs are tied to specific pods, ensuring that the data persists across restarts.



In a StatefulSet's updateStrategy, what is the purpose of the 'partition' value?
- It specifies the number of replicas
- It determines the number of pods to update simultaneously
- It indicates the starting point for a rolling update (Correct)
- It defines the version of the application to deploy


Explanation:
In a StatefulSet, the updateStrategy field defines how updates to the StatefulSet are managed. The partition value is a part of the rolling update strategy and it controls how many pods will be updated during a rolling update, by indicating the starting point for the update.

Here’s how the partition works in more detail:

Partition Value: The partition specifies the pod index up to which updates will not occur. In other words, pods with an index less than the partition value will not be updated during the rolling update, and only the pods with an index greater than or equal to the partition value will be updated.

If partition = 0, it means that no pods will be updated initially, and the update will start from pod 0.
If partition = 2, it means that only pods 2, 3, etc., will be updated, while pods 0 and 1 will remain in their current state.
As the update progresses, the partition value is typically decreased to allow the update to proceed to the next set of pods.
The partition value is especially useful when you need to control the pace of the update or avoid disruption in critical parts of your application by holding back the update on certain pods.

Example:
Consider a StatefulSet with 5 replicas (pod-0, pod-1, pod-2, pod-3, and pod-4). If the partition is set to 2, the rolling update will start from pod-2 and update the remaining pods (pod-2, pod-3, pod-4). Pods pod-0 and pod-1 will not be updated during this process.


      updateStrategy:
        type: RollingUpdate
        rollingUpdate:
          partition: 2
   
How are pods in a Kubernetes StatefulSet named?
- With randomized names
- With the StatefulSet name followed by a unique identifier
- With the same name as the StatefulSet
- Sequentially, starting from zero and prefixed with the StatefulSet name (Corrrect)

Explanation

he correct answer is:

Sequentially, starting from zero and prefixed with the StatefulSet name
Explanation:
In Kubernetes, when you create a StatefulSet, the pods are named sequentially based on the name of the StatefulSet followed by a unique index starting from 0. This allows each pod to have a stable, unique identity, which is crucial for stateful applications.

The naming pattern for pods in a StatefulSet is as follows:

php
Copiar código
<statefulset-name>-<ordinal-index>
For example, if the StatefulSet is named my-stateful-app and it has 3 replicas, the pods will be named:

my-stateful-app-0
my-stateful-app-1
my-stateful-app-2
These names are sequential and are based on the index value (0, 1, 2, etc.). This gives each pod in the StatefulSet a stable identity, even if they are rescheduled or recreated.

****Importante****: Estudiar sobre los rollingUpdates


Kubernetes NetworkPolicies - Study Tips
For the KCNA Examination, you need to be aware of the role of Network Policies and that policies are cumulative. If you apply multiple NetworkPolicies to a set of pods, the policies are added together.

The effective policy is the union of all the individual policies. This approach ensures that if any policy allows a particular type of traffic, that traffic is allowed.


<h2>Network Policy</h2>

![image](https://github.com/user-attachments/assets/9df99681-3bdc-4cd5-84bc-7886b7e29fed)


If you want to control traffic flow at the IP address or port level for TCP, UDP, and SCTP protocols, then you might consider using Kubernetes NetworkPolicies for particular applications in your cluster. NetworkPolicies are an application-centric construct which allow you to specify how a pod is allowed to communicate with various network "entities" (we use the word "entity" here to avoid overloading the more common terms such as "endpoints" and "services", which have specific Kubernetes connotations) over the network. NetworkPolicies apply to a connection with a pod on one or both ends, and are not relevant to other connections.

The entities that a Pod can communicate with are identified through a combination of the following three identifiers:

Other pods that are allowed (exception: a pod cannot block access to itself)
Namespaces that are allowed
IP blocks (exception: traffic to and from the node where a Pod is running is always allowed, regardless of the IP address of the Pod or the node)
When defining a pod- or namespace-based NetworkPolicy, you use a selector to specify what traffic is allowed to and from the Pod(s) that match the selector.

Meanwhile, when IP-based NetworkPolicies are created, we define policies based on IP blocks (CIDR ranges).


     apiVersion: networking.k8s.io/v1
     kind: NetworkPolicy
     metadata:
       name: test-network-policy
       namespace: default
     spec:
       podSelector:
         matchLabels:
           role: db
       policyTypes:
       - Ingress
       - Egress
       ingress:
       - from:
         - ipBlock:
             cidr: 172.17.0.0/16
             except:
             - 172.17.1.0/24
         - namespaceSelector:
             matchLabels:
               project: myproject
         - podSelector:
             matchLabels:
               role: frontend
         ports:
         - protocol: TCP
           port: 6379
       egress:
       - to:
         - ipBlock:
             cidr: 10.0.0.0/24
         ports:
         - protocol: TCP
           port: 5978


Note:
POSTing this to the API server for your cluster will have no effect unless your chosen networking solution supports network policy.
Mandatory Fields: As with all other Kubernetes config, a NetworkPolicy needs apiVersion, kind, and metadata fields. For general information about working with config files, see Configure a Pod to Use a ConfigMap, and Object Management.

spec: NetworkPolicy spec has all the information needed to define a particular network policy in the given namespace.

podSelector: Each NetworkPolicy includes a podSelector which selects the grouping of pods to which the policy applies. The example policy selects pods with the label "role=db". An empty podSelector selects all pods in the namespace.

policyTypes: Each NetworkPolicy includes a policyTypes list which may include either Ingress, Egress, or both. The policyTypes field indicates whether or not the given policy applies to ingress traffic to selected pod, egress traffic from selected pods, or both. If no policyTypes are specified on a NetworkPolicy then by default Ingress will always be set and Egress will be set if the NetworkPolicy has any egress rules.

ingress: Each NetworkPolicy may include a list of allowed ingress rules. Each rule allows traffic which matches both the from and ports sections. The example policy contains a single rule, which matches traffic on a single port, from one of three sources, the first specified via an ipBlock, the second via a namespaceSelector and the third via a podSelector.

egress: Each NetworkPolicy may include a list of allowed egress rules. Each rule allows traffic which matches both the to and ports sections. The example policy contains a single rule, which matches traffic on a single port to any destination in 10.0.0.0/24.


****Importante***** 

![image](https://github.com/user-attachments/assets/78ceb885-4c40-45bb-b38d-d65df5eee642)


Commands: 

kubectl get networkpolicy: obtiene las networks policys



Questions

What is the primary function of NetworkPolicies in Kubernetes?
- To automate pod deployment
- To classify Pods as isolated and control their communication (Correct)
- To increase the storage capacity of pods
- To monitor pod performance


In Kubernetes, what does an 'Ingress' rule in a NetworkPolicy define?
- The traffic allowed to exit from pods
- The storage limits for pods
- The traffic allowed to enter to pods (Correct)
- The scheduling preferences for pods


How does a NetworkPolicy in Kubernetes become effective?
- By default, it is effective immediately after the cluster creation  (Correct)
- It must be linked to a specific service
- It becomes effective after it is applied
- Only after restarting the Kubernetes cluster


When a pod is created using kubectl run in Kubernetes, what type of label is automatically assigned to it?
- namespace:
- run: (Correct)
- pod:
- service:

Explanation

When you create a pod using kubectl run in Kubernetes, a label called run is automatically assigned to the pod. The label key will be run, and the value will be the name of the pod or deployment.
For example, if you run:
kubectl run mypod --image=nginx
A label run=mypod will automatically be applied to the pod. You can check the labels using kubectl get pods --show-labels.


Which component is essential for the enforcement of NetworkPolicies in Kubernetes?
- The Kubernetes API server
- A Container Runtime Interface (CRI) plugin
- A Container Network Interface (CNI) plugin (Correct)
- The Kubernetes scheduler

NetworkPolicies in Kubernetes control the communication between pods based on rules like source, destination, and ports. However, these policies are enforced by the CNI (Container Network Interface) plugin.
The CNI plugin is responsible for configuring network connectivity and enforcing the network policies that are defined in Kubernetes. It ensures that traffic is allowed or blocked between pods according to the rules specified in the NetworkPolicy.



What is the default behaviour of a pod in a Kubernetes cluster that does not have any NetworkPolicies applied to it?
- It cannot send or receive any traffic
- It can only communicate within its own namespace 
- It can send and receive traffic from any source (Correct)
- It is isolated from the rest of the cluster


Explanation:

The correct answer is: It can send and receive traffic from any source

In Kubernetes, if no NetworkPolicies are applied to a pod, it is not isolated by default. This means the pod is permissive, and it can send and receive traffic from any other pod, service, or external source. The absence of NetworkPolicies implies that Kubernetes does not enforce any restrictions on network traffic between pods or namespaces.


How do NetworkPolicies behave when multiple policies are applied to a set of pods in Kubernetes?
- They cancel each other out, and none are applied
- Only the most restrictive policy is applied
- Policies are additive and cumulative in effect  (Correct)
- Only the least restrictive policy is applied

Explanation:

The correct answer is: Policies are additive and cumulative in effect

When multiple NetworkPolicies are applied to a set of pods in Kubernetes, they are not mutually exclusive or individually prioritized (i.e., the most restrictive or least restrictive is not automatically applied). Instead, they are additive and cumulative — all the policies are considered, and the final result is the combination of all the rules from each applied policy.



<h2>Kubernetes Pod Disruption Budgets</h2>

Kubernetes Pod Disruption Budgets - Study Tips
For the KCNA examination, a general understanding of Pod Disruption Budgets is required, specific on the implementation and use-cases should be considered as informational only in the following video.


Reliability with examples pods with replicas

Se borraron de un nodo, sin embargo mantiene sus replicas en el worker 2, incluso si la boran
![image](https://github.com/user-attachments/assets/bd62c9fe-366e-4c88-b5d8-4e03d131a601)

![image](https://github.com/user-attachments/assets/b07df307-7ed5-41ac-ab3d-5e49996027b4)


Comandos

- kubectl cordon worker-1 && kubectl delete pod/nginx-77b4fdf86c-bgx4z pod/nginx-77b4fdf86c-7srbx

  kubectl cordon worker-1
  Este comando marca el nodo worker-1 como "cordoneado". Cuando un nodo está cordoneado, Kubernetes evita que se asignen nuevos pods a ese nodo, pero no afecta a los pods que ya están en ejecución en el nodo. Es una manera de evitar que más cargas de trabajo lleguen a ese nodo mientras se pueden seguir ejecutando los pods existentes.
  
  cordon: Marca el nodo como no programable (no puede aceptar nuevos pods).
  worker-1: Es el nombre del nodo que estás marcando como cordoneado.
  2. kubectl delete pod/nginx-77b4fdf86c-bgx4z pod/nginx-77b4fdf86c-7srbx
  Este comando elimina dos pods específicos del clúster de Kubernetes:
  
  kubectl delete pod: Elimina uno o más pods del clúster.
  nginx-77b4fdf86c-bgx4z y nginx-77b4fdf86c-7srbx: Son los nombres de los pods específicos que estás eliminando. Es posible que estos pods sean parte de un despliegue de Nginx.
  Cuando se elimina un pod que forma parte de un Deployment (como en este caso parece ser un pod de Nginx), el controlador de replicación del Deployment creará nuevos pods automáticamente para reemplazar los eliminados, garantizando que el número de réplicas del Deployment se mantenga.
  
  En resumen:
  kubectl cordon worker-1: Marca al nodo worker-1 como no disponible para nuevos pods.
  kubectl delete pod ...: Elimina dos pods específicos de Nginx.




-  kubectl drain worker-2 --delete-emptydir-data=true --ignore-daemonsets=true


   El comando kubectl drain se utiliza en Kubernetes para preparar un nodo para su mantenimiento, lo que implica mover todos los pods que están en ese nodo a otros nodos disponibles dentro del clúster. A diferencia de kubectl cordon, que solo 
   evita que se programen nuevos pods en el nodo, kubectl drain intenta reubicar los pods que están en el nodo de forma activa. Es común usar kubectl drain cuando se necesita realizar mantenimiento en un nodo, como actualizarlo o apagarlo.
   
   Desglose del comando: kubectl drain worker-2 --delete-emptydir-data=true --ignore-daemonsets=true

  kubectl drain: Este comando intenta evacuar el nodo especificado (worker-2 en este caso) moviendo todos los pods programados en ese nodo a otros nodos disponibles.

  El nodo se marca como no programable (equivalente a cordon) para que no se asignen nuevos pods mientras se realiza el proceso de drenado.
  worker-2: Es el nombre del nodo que estás drenando (en este caso, worker-2).
  
  --delete-emptydir-data=true: Esta opción hace que los datos almacenados en los volúmenes de tipo emptyDir de los pods que están en el nodo también sean eliminados cuando esos pods son evacuados y eliminados. Los volúmenes emptyDir se crean cuando un pod se ejecuta y se eliminan cuando el pod es destruido. Si esta opción no se especifica o se pone a false, los datos de los volúmenes emptyDir se conservarían.
  
  --ignore-daemonsets=true: Por defecto, kubectl drain no moverá ni eliminará los pods de los DaemonSets. Los DaemonSets son objetos que aseguran que haya un pod ejecutándose en cada nodo (por ejemplo, para tareas de logging o monitoring). Esta opción le dice a Kubernetes que ignore los pods gestionados por DaemonSets durante el drenado, lo que significa que esos pods no se eliminarán ni se moverán a otro nodo. Si no usas esta opción, los pods de los DaemonSets también se moverían o eliminarían, lo cual generalmente no es lo deseado.


- kubectl uncordon controlplane: El comando kubectl uncordon se utiliza en Kubernetes para marcar un nodo previamente cordoneado como "disponible" nuevamente para programar pods. Esto significa que, después de ejecutar uncordon, Kubernetes permitirá que nuevos pods se asignen a ese nodo.
   
- kubectl get pdb: 

POD DISRUPTION BUDGET

Un Pod Disruption Budget (PDB) es un recurso de Kubernetes que establece el número mínimo de pods que deben seguir disponibles durante una interrupción: 
- Las interrupciones pueden ser voluntarias, como la escalación de nodos o las operaciones de mantenimiento.
- Las interrupciones también pueden ser involuntarias, como los fallos de hardware o los bloqueos del sistema.
- Los PDBs ayudan a: Mantener la estabilidad de la aplicación, Minimizar el tiempo de inactividad, Garantizar la alta disponibilidad de las aplicaciones. 
- Los PDBs son útiles en diversas industrias, como el comercio electrónico, donde pueden ayudar a garantizar que un número mínimo de pods permanezca disponible durante las actualizaciones.

![image](https://github.com/user-attachments/assets/abb5086f-ba5a-41fd-a7f1-514bdcfad5f6)


- kubectl create pdb my-nginx-test --selector=app=my-nginx-test --min-available=2: estamos creando un Pod Disruption Budget


****Importante*****
Specifying a Disruption Budget for your Application: https://kubernetes.io/docs/tasks/run-application/configure-pdb/
Leer sobre este link: https://kubernetes.io/es/docs/tasks/run-application/configure-pdb/
Leer sobre esto: https://kubernetes.io/docs/reference/kubectl/generated/kubectl_drain/
Leer: A Hands-On Guide to Kubernetes Pod Disruption Budget (PDB) - https://medium.com/@muppedaanvesh/a-hand-on-guide-to-kubernetes-pod-disruption-budget-pdb-%EF%B8%8F-ebe3155a4b7c


Questions

What is the primary purpose of Pod Disruption Budgets (PDBs) in Kubernetes?
- To automate pod scaling
- To ensure high availability during voluntary disruptions (Correct)
- To balance load across multiple nodes
- To monitor pod performance



In the context of Kubernetes, what does the term 'voluntary disruptions' refer to?
- Unplanned outages like hardware failures
- Intentional actions like maintenance or upgrades (Correct)
- Automatic pod scaling based on load
- Network interruptions external to the cluster


Which Kubernetes command is used to make a node un-schedulable?
- kubectl drain
- kubectl delete
- kubectl cordon (Correct)
- kubectl create


What happens when you use the 'kubectl drain' command on a node?
- The node is deleted from the cluster
- It marks the node as schedulable
- It removes all pods from the node (Correct)
- It automatically creates a new node


Explanation

When you use the kubectl drain command on a node, the correct behavior is:

It removes all pods from the node.
Here’s a breakdown of what happens when you run kubectl drain on a node:

Evacuates Pods: The command removes all pods from the node by either deleting them or migrating them to other nodes in the cluster. Kubernetes will attempt to safely evict the pods running on that node while respecting PodDisruptionBudgets (PDBs) to ensure that a minimum number of pods are available during disruptions.
Respecting DaemonSets: By default, kubectl drain does not affect pods managed by DaemonSets. If you want to drain a node but still allow DaemonSet pods to run, you can use the --ignore-daemonsets=true option.
Marks Node as Unschedulable: The node is marked as unschedulable (equivalent to kubectl cordon), meaning Kubernetes will not schedule any new pods on it until it is uncordoned with the kubectl uncordon command.



What is the difference between PDBs and replicas in Kubernetes?
- PDBs automate scaling, while replicas ensure high availability
- Replicas ensure availability under normal operations, while PDBs protect during disruptions (Correct)
- Replicas manage storage, while PDBs manage networking
- There is no difference; they are the same



How does a Pod Disruption Budget improve application stability during maintenance?
- By increasing the number of replicas automatically
- By preventing the eviction of a certain number of pods (Correct)
- By redistributing pods across available nodes
- By upgrading the Kubernetes version



<h2>Kubernetes Security</h2>

Kubernetes Security - Study Tips
For the KCNA exam, the following considerations -

Awareness of Security Tools and their function including Falco and Open Policy Agent
Knowledge that Kubescape can be used for hardening to NSA and CISA standards
OpenID Connect and it's purpose, be aware that the exam may shorten this to OIDC
Legacy: Although Pod Security Policies are deprecated, this was previously a common question in the exam and you should be aware that Pod Security Policies manage Clusters and Namespaces at runtime
The 4C's of Cloud Native Security


Tools for support the security in Kubernetes

![image](https://github.com/user-attachments/assets/4d59f0dc-415d-40c1-8649-e31e622e9f08)


Leer este ducumento: https://kubernetes.io/docs/tasks/configure-pod-container/security-context/


Comands

El comando kubectl replace --force -f ubuntu_secure.yaml es utilizado en Kubernetes para reemplazar un recurso (como un pod, deployment, service, etc.) que ya existe en el clúster. Vamos a desglosar el comando:
* kubectl: Es la herramienta de línea de comandos de Kubernetes. Permite interactuar con el clúster de Kubernetes y administrar sus recursos.
* replace: Este subcomando reemplaza un recurso que ya existe en el clúster con el contenido del archivo proporcionado. Si el recurso no existe, se obtiene un error.
*  --force: Esta opción se usa para forzar el reemplazo de un recurso aunque el clúster no pueda realizar un "rolling update" o no haya una comparación directa. Se utiliza para actualizar el recurso incluso si eso requiere eliminar y recrear el * objeto de forma abrupta. Advertencia: Usar --force puede causar una interrupción temporal del servicio, ya que el recurso será destruido y luego recreado.
* -f ubuntu_secure.yaml: Especifica el archivo de definición de recursos de Kubernetes, en este caso ubuntu_secure.yaml. Este archivo debe contener la descripción del recurso a crear o reemplazar en formato YAML.

<h4>Diferencias Claves</h4>

<table border="1">
  <thead>
    <tr>
      <th>Característica</th>
      <th>kubectl apply</th>
      <th>kubectl replace</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Enfoque</td>
      <td>Declarativo (gestiona el estado deseado)</td>
      <td>Imperativo (reemplaza el recurso completamente)</td>
    </tr>
    <tr>
      <td>Manejo de recursos existentes</td>
      <td>Actualiza los recursos existentes o los crea si no existen</td>
      <td>Reemplaza completamente los recursos existentes</td>
    </tr>
    <tr>
      <td>Control de versiones</td>
      <td>Mantiene un historial de cambios (para aplicar cambios incrementales)</td>
      <td>No mantiene historial de cambios, sobrescribe el recurso por completo</td>
    </tr>
    <tr>
      <td>Uso en equipos múltiples</td>
      <td>Más adecuado para entornos colaborativos y entornos dinámicos</td>
      <td>Puede ser útil para cambios drásticos o restauración completa</td>
    </tr>
    <tr>
      <td>Acción sobre recursos no existentes</td>
      <td>Crea el recurso si no existe</td>
      <td>Devuelve un error si el recurso no existe</td>
    </tr>
    <tr>
      <td>Aplicación de cambios</td>
      <td>Realiza cambios incrementales, solo lo que es necesario</td>
      <td>Reemplaza el recurso completo, destruye el recurso existente y lo recrea</td>
    </tr>
  </tbody>
</table>




Ejemplo de archivo:

     apiVersion: v1
     kind: Pod
     metadata:
       creationTimestamp: null
       labels:
         run: ubuntu
       name: ubuntu
     spec:
       securityContext:
         runAsUser: 1000
         runAsGroup: 1000
       containers:
       - args:
         - sleep
         - infinity
         image: spurin/rootshell:latest
         name: ubuntu
         resources: {}
         securityContext:
           allowPrivilegeEscalation: false
       dnsPolicy: ClusterFirst
       restartPolicy: Always
     status: {}


dentro de las ventajas podemos agregar:

securityContext: 
  allowPrivilegeEscalation: false

Puesto que la opción allowPrivilegeEscalation: false evita que un proceso dentro del contenedor pueda elevar sus privilegios (es decir, que no pueda obtener privilegios más altos de los que tiene inicialmente). En otras palabras, no permite que un contenedor ejecute procesos como usuario root o adquiera privilegios adicionales mediante técnicas como setuid o setgid.


![image](https://github.com/user-attachments/assets/f1ea8bbd-c9c8-41ae-bd9f-f15d2a21ed61)

Antes se usaba Pod Security Policys, sin embargo fueron removidas en versiones posteriores. 

Pod Security Policies
Removed feature
PodSecurityPolicy was deprecated in Kubernetes v1.21, and removed from Kubernetes in v1.25.
Instead of using PodSecurityPolicy, you can enforce similar restrictions on Pods using either or both:

Pod Security Admission
a 3rd party admission plugin, that you deploy and configure yourself
For a migration guide, see Migrate from PodSecurityPolicy to the Built-In PodSecurity Admission Controller. For more information on the removal of this API, see PodSecurityPolicy Deprecation: Past, Present, and Future.

If you are not running Kubernetes v1.31, check the documentation for your version of Kubernetes.


Kubernetes Admission Controllers

What are they?
An admission controller is a piece of code that intercepts requests to the Kubernetes API server prior to persistence of the object, but after the request is authenticated and authorized.

Admission controllers may be validating, mutating, or both. Mutating controllers may modify objects related to the requests they admit; validating controllers may not.

Admission controllers limit requests to create, delete, modify objects. Admission controllers can also block custom verbs, such as a request connect to a Pod via an API server proxy. Admission controllers do not (and cannot) block requests to read (get, watch or list) objects.

The admission controllers in Kubernetes 1.31 consist of the list below, are compiled into the kube-apiserver binary, and may only be configured by the cluster administrator. In that list, there are two special controllers: MutatingAdmissionWebhook and ValidatingAdmissionWebhook. These execute the mutating and validating (respectively) admission control webhooks which are configured in the API.

Admission control phases
The admission control process proceeds in two phases. In the first phase, mutating admission controllers are run. In the second phase, validating admission controllers are run. Note again that some of the controllers are both.

If any of the controllers in either phase reject the request, the entire request is rejected immediately and an error is returned to the end-user.

Finally, in addition to sometimes mutating the object in question, admission controllers may sometimes have side effects, that is, mutate related resources as part of request processing. Incrementing quota usage is the canonical example of why this is necessary. Any such side-effect needs a corresponding reclamation or reconciliation process, as a given admission controller does not know for sure that a given request will pass all of the other admission controllers.

Why do I need them?
Several important features of Kubernetes require an admission controller to be enabled in order to properly support the feature. As a result, a Kubernetes API server that is not properly configured with the right set of admission controllers is an incomplete server and will not support all the features you expect.

How do I turn on an admission controller?
The Kubernetes API server flag enable-admission-plugins takes a comma-delimited list of admission control plugins to invoke prior to modifying objects in the cluster. For example, the following command line enables the NamespaceLifecycle and the LimitRanger admission control plugins:

kube-apiserver --enable-admission-plugins=NamespaceLifecycle,LimitRanger ...
Note:
Depending on the way your Kubernetes cluster is deployed and how the API server is started, you may need to apply the settings in different ways. For example, you may have to modify the systemd unit file if the API server is deployed as a systemd service, you may modify the manifest file for the API server if Kubernetes is deployed in a self-hosted way.
How do I turn off an admission controller?
The Kubernetes API server flag disable-admission-plugins takes a comma-delimited list of admission control plugins to be disabled, even if they are in the list of plugins enabled by default.

kube-apiserver --disable-admission-plugins=PodNodeSelector,AlwaysDeny ...
Which plugins are enabled by default?
To see which admission plugins are enabled:

kube-apiserver -h | grep enable-admission-plugins

![image](https://github.com/user-attachments/assets/729bc938-e945-4363-9889-f8036adcda1b)




Others definitions for Admission Controllers in spanish

Un Admission Controller (Controlador de Admisión) en Kubernetes es un componente que intercepta y valida las solicitudes de creación, modificación o eliminación de recursos dentro del clúster antes de que estas sean persistidas en la API de Kubernetes. Los Admission Controllers permiten que las políticas de seguridad, auditoría y validación sean aplicadas de manera centralizada en el clúster.

¿Cómo funcionan los Admission Controllers?
Cuando una solicitud se realiza a la API de Kubernetes (por ejemplo, para crear o modificar un Pod, Deployment, etc.), Kubernetes pasa la solicitud a través de una serie de Admission Controllers antes de que la solicitud sea finalmente aceptada o rechazada.

El flujo típico de una solicitud es:

El cliente (por ejemplo, kubectl) envía una solicitud al API Server de Kubernetes.
El API Server procesa la solicitud y la pasa a través de los Admission Controllers.
Los Admission Controllers pueden:
Validar: Comprobar si la solicitud cumple con ciertas políticas o reglas.
Mutar: Modificar la solicitud antes de que se persista (por ejemplo, añadiendo etiquetas, volúmenes, etc.).
Después de pasar por los Admission Controllers, la solicitud es persistida en la base de datos de Kubernetes (etcd), y el recurso es creado o actualizado.
Tipos de Admission Controllers
Los Admission Controllers pueden clasificarse en dos categorías principales:

Validación:

Validan las solicitudes de recursos para asegurarse de que cumplen con las reglas de la política del clúster (por ejemplo, comprobar que un contenedor no tiene privilegios de root o que el tamaño de un pod es adecuado).
Si una solicitud no pasa la validación, es rechazada.
Mutación:

Modifican las solicitudes antes de que se apliquen, agregando o modificando configuraciones de los recursos.
Esto se utiliza para agregar automáticamente etiquetas, anotaciones, volúmenes, configuraciones de seguridad, etc.
Ejemplos de Admission Controllers comunes:
NamespaceLifecycle:

Se asegura de que los objetos no puedan crearse en un espacio de nombres (namespace) que ha sido eliminado o marcado para su eliminación.
LimitRanger:

Aplica límites de recursos a los contenedores en un Pod (por ejemplo, limita la cantidad de CPU o memoria que puede usar un contenedor).
ResourceQuota:

Aplica límites a los recursos que se pueden consumir dentro de un namespace específico (por ejemplo, el número máximo de Pods, CPU, memoria, etc.).
PodSecurityPolicy (desaprobado en versiones posteriores de Kubernetes, reemplazado por PodSecurity):

Asegura que los Pods cumplan con políticas de seguridad, como la prohibición de ejecutar contenedores como root, la obligación de usar un usuario no privilegiado, etc.
NodeRestriction:

Restringe el acceso de los nodos a solo sus propios recursos. Por ejemplo, un nodo no podrá crear Pods en otro nodo, ni modificar la configuración de otros nodos.
SecurityContextDeny:

Rechaza cualquier Pod que tenga un securityContext que permita privilegios elevados, como ejecutar como root.
MutatingAdmissionWebhook y ValidatingAdmissionWebhook:

Permiten integrar webhooks externos que se pueden usar para realizar validaciones o mutaciones más complejas y específicas que no están cubiertas por los Admission Controllers integrados de Kubernetes.
Los webhooks permiten a los desarrolladores crear políticas personalizadas que se apliquen a las solicitudes de recursos.
¿Dónde se configuran los Admission Controllers?
En Kubernetes, los Admission Controllers son parte del API Server. Se pueden habilitar o deshabilitar al configurar el kube-apiserver (generalmente en el archivo de configuración del clúster o al ejecutar el servidor). Existen dos tipos de Admission Controllers que se pueden habilitar:

Mutating Admission Controllers: Modifican las solicitudes.
Validating Admission Controllers: Validan las solicitudes.
¿Por qué son importantes?
Seguridad:
Los Admission Controllers son esenciales para aplicar políticas de seguridad dentro de Kubernetes. Por ejemplo, puedes usar un Admission Controller para asegurarte de que los Pods no se ejecuten como root o que no puedan usar privilegios elevados.
Automatización:
Pueden automatizar tareas repetitivas o necesarias para mantener la coherencia en el clúster. Por ejemplo, agregar etiquetas o anotaciones automáticamente a todos los recursos que se crean.
Cumplimiento de políticas:
Garantizan que las políticas del clúster sean aplicadas correctamente a nivel de configuración y comportamiento de los recursos, asegurando el cumplimiento de estándares internos o externos (como regulaciones de seguridad).
Ejemplo de uso de un Admission Controller
Imagina que quieres asegurarte de que todos los Pods creados en tu clúster no se ejecuten como root. Para ello, podrías habilitar el Admission Controller PodSecurityPolicy (aunque este controlador será deprecado en futuras versiones, y se recomienda utilizar el controlador PodSecurity en su lugar).

Un ejemplo de configuración de política de seguridad que impide ejecutar Pods como root sería algo así:


    apiVersion: policy/v1beta1
    kind: PodSecurityPolicy
    metadata:
      name: no-root
    spec:
      privileged: false
      runAsUser:
        rule: MustRunAsNonRoot

        
Esta política se aplicaría a los Pods creados en el clúster a través de un Admission Controller, asegurando que no se permitan Pods que se ejecuten con privilegios de root.
