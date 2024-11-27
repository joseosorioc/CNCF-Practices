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
