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
      --timestamps[=false]: Include timestamps on each line in the log output
