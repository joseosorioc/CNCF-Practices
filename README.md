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


The Kyverno (Es un proyecto graduado de la CNCF ***Tenerlo en cuenta*** )


The Kyverno project provides a comprehensive set of tools to manage the complete Policy-as-Code (PaC) lifecycle for Kubernetes and other cloud native environments.
Kyverno policies are declarative YAML resources and no new language is required. Kyverno enables use of familiar tools such as kubectl, git, and kustomize to manage policies. Kyverno supports JMESPath and the Common Expressions Language (CEL) for efficient handling of complex logic.


Kyverno es una herramienta de política de seguridad y gestión de configuraciones para Kubernetes. Es un admission controller que permite a los administradores de Kubernetes definir, aplicar y verificar políticas de seguridad, cumplimiento y gobernanza en recursos dentro del clúster de manera fácil y declarativa.


Open Policy Agent  (Es un proyecto graduado de la CNCF ***Tenerlo en cuenta*** )


¿Qué es Open Policy Agent (OPA)?
OPA es un motor de políticas general-purpose que puede integrarse con cualquier sistema que necesite políticas, no solo Kubernetes. Funciona evaluando políticas que se definen mediante el lenguaje de políticas Rego y tomando decisiones en función de los datos proporcionados por el sistema.

OPA puede ser utilizado para:

- Validación de políticas de seguridad (por ejemplo, si un contenedor puede ejecutarse como root).
- Control de acceso basado en roles (RBAC).
- Auditoría de cumplimiento normativo.
- Decisiones de enrutamiento dinámico en micro.


Falco (Es un proyecto graduado de la CNCF ***Tenerlo en cuenta*** )

Falco is a cloud-native security tool designed for Linux systems. It employs custom rules on kernel events, which are enriched with container and Kubernetes metadata, to provide real-time alerts. Falco helps you gain visibility into abnormal behavior, potential security threats, and compliance violations, contributing to comprehensive runtime security.

Representacion de un conjunto de politicas en Kubernetes

![image](https://github.com/user-attachments/assets/1b1f9ce7-88b0-4f9e-85ab-468b296a0ea0)



Kubescape
An open-source Kubernetes security platform for your clusters, CI/CD pipelines, and IDE that seperates out the security signal from the scanner noise
Kubescape is an open-source Kubernetes security platform, built for use in your day-to-day workflow, by fitting into your clusters, CI/CD pipelines and IDE. It serves as a one-stop-shop for Kuberenetes security and includes vulnerability and misconfiguration scanning.


You can run scans via the CLI, or add the Kubescape Helm chart, which gives an in-depth view of what is going on in the cluster.
Kubescape includes misconfiguration and vulnerability scanning as well as risk analysis and security compliance indicators. All results are presented in context and users get many cues on what to do based on scan results.Targeted at the DevSecOps practitioner or platform engineer, it offers an easy-to-use CLI interface, flexible output formats, and automated scanning capabilities. It saves Kubernetes users and admins precious time, effort, and resources.
Kubescape scans clusters, YAML files, and Helm charts. It detects misconfigurations according to multiple frameworks (including NSA-CISA, MITRE ATT&CK® and the CIS Benchmark).
Kubescape was created by ARMO and is a Cloud Native Computing Foundation (CNCF) sandbox project.

OpenID

OpenID es un estándar de autenticación y una tecnología de identidad descentralizada que permite a los usuarios autenticarse en diferentes sitios web y aplicaciones usando una única identidad, sin necesidad de crear nuevas credenciales para cada servicio. El objetivo principal de OpenID es facilitar un inicio de sesión único (SSO, por sus siglas en inglés) para que los usuarios no tengan que gestionar múltiples contraseñas en diferentes plataformas.

Fue creado por la Open ID Foundation

The OpenID Foundation’s vision is to help people assert their identity wherever they choose. And our mission is to lead the global community in creating identity standards that are secure, interoperable, and privacy-preserving. Founded in 2007, the OpenID Foundation (OIDF) is a non-profit open standards body developing identity and security specifications that serve billions of consumers across millions of applications.


![image](https://github.com/user-attachments/assets/eb5286cf-ac1d-4456-ab1d-1966d7a0ad6a)



<h2>Importantisimo aprenderse este diagrama (Obligatorio recordarlo)</h2>

For awareness and also for the purposes of the KCNA exam, you should be aware of the 4C’s of Cloud Native Security, namely Cloud, Cluster, Container, Code.

Each endpoint acts as a layer from the outside-in and is a security best practice in Cloud Native Computing.

Each subsequent layer acts as a reinforcement for the layer within. For example, Code would benefit from the security implementations of Container, Cluster and Cloud respectively.

See the following image with a friendly poem to help you remember this!

![image](https://github.com/user-attachments/assets/dc3e2816-df17-413a-b155-fb2a9d8bae24)



Questions

What Kubernetes feature defines privilege and access control settings for a Pod or Container?
- Security Admission Controller
- Security Contexts (Correct)
- Pod Security Policies
- Cluster Policies


What is the primary function of Admission Controllers in Kubernetes?
- To orchestrate container deployment
- To define network policies
- To act as gatekeepers for pod creation and modification (Correct)
- To monitor pod performance


What Kubernetes security feature was deprecated in version 1.21 and removed in version 1.25?
- Security Contexts
- Pod Admission Controllers
- Pod Security Policies  (Correct)
- Kubernetes Service Accounts


Which tool is an open-source runtime security project that integrates with Kubernetes for identifying abnormal behavior and potential security threats?
- Kubescape
- Kyverno
- Falco  (Correct)
- Open Policy Agent

The correct answer is: Falco

Explanation:
Falco is an open-source runtime security tool that integrates with Kubernetes and helps identify abnormal behavior and potential security threats in real-time. It uses a system call monitoring approach to detect suspicious activities, such as unexpected file access, privilege escalation, or unauthorized processes running on your containers and Kubernetes clusters. It is often used for security monitoring and threat detection within Kubernetes environments by monitoring kernel system calls and generating alerts when it detects abnormal behavior.



Which protocol is recommended for enhanced authentication in large-scale Kubernetes deployments?
- SAML
- OAuth 2.0
- LDAP
- OpenID Connect (OIDC)  (Correct)

The correct answer is: OpenID Connect (OIDC)

Explanation:
OpenID Connect (OIDC) is the recommended protocol for enhanced authentication in large-scale Kubernetes deployments. It is an identity layer built on top of OAuth 2.0 and is commonly used for authenticating users in cloud-native environments, including Kubernetes clusters.


Why OIDC?

Standardized and Flexible: OIDC is widely adopted and supported by cloud identity providers such as Google, AWS, Azure, and Okta, making it easy to integrate with your existing identity and access management systems.
User Authentication: It allows Kubernetes to authenticate users via an identity provider (IdP), such as Google or Active Directory, using tokens (JWT tokens) that are verified by Kubernetes.
Scalable: OIDC is well-suited for large-scale environments because it supports centralized identity management and single sign-on (SSO), streamlining the authentication process.
Secure: It integrates with modern security protocols, providing robust mechanisms like token-based authentication and support for multi-factor authentication (MFA).



Which tool is designed for vulnerability and misconfiguration scanning in Kubernetes clusters?
- Falco
- Kyverno
- Open Policy Agent
- Kubescape  (Correct)


The correct answer is:

Kubescape

Explanation:
Kubescape is a tool designed specifically for vulnerability scanning and misconfiguration detection in Kubernetes clusters. It scans Kubernetes configurations (including YAML files), Helm charts, and Kubernetes resources for potential security vulnerabilities, misconfigurations, and policy violations.
It focuses on identifying potential risks and security issues in the way Kubernetes resources are configured, such as exposed ports, insecure pod configurations, or improper role-based access control (RBAC) settings.




Which of the following is a common option for Pod Admission Controllers in Kubernetes?
- Kyverno and Open Policy Agent Gatekeeper
- Helm and Kustomize
- Docker and Containerd
- Grafana and Prometheus


The correct answer is:

Kyverno and Open Policy Agent Gatekeeper

Explanation:

- Pod Admission Controllers in Kubernetes are mechanisms that intercept requests to the Kubernetes API server before the requests are persisted, allowing administrators to enforce policies, modify objects, or reject requests based on certain criteria.

- Kyverno and Open Policy Agent Gatekeeper (OPA Gatekeeper) are both policy engines used for enforcing policies in Kubernetes, including policies on pods and other resources. They act as Admission Controllers, which allow you to define rules and policies for resources at the time they are created, updated, or deleted. These tools are specifically designed for policy validation and can prevent misconfigurations and enforce security standards in a Kubernetes cluster.

- Kyverno: A Kubernetes-native policy engine that can validate, mutate, and generate Kubernetes resources. It supports both the admission control process and the enforcement of policies across various resources, including pods.

- OPA Gatekeeper: A policy engine built on Open Policy Agent that helps enforce policies in Kubernetes by using Rego (a declarative language). Gatekeeper works as an Admission Controller to evaluate and enforce policies for resources in the cluster, including pods.


In the Kubernetes security context example, what is the outcome of setting allowPrivilegeEscalation: false in the container's security context?
- It allows containers to run as root
- It prevents containers from accessing cluster resources 
- It prevents the escalation of privileges in the container (Correct)
- It enables network policies for the container


Which sequence correctly represents the 4C's of Cloud Native Security?
- Containers, Clusters, Cloud, Code
- Cloud, Clusters, Containers, Code (Correct)
- Code, Containers, Cloud, Clusters
- Clusters, Containers, Code, Cloud



<h2>Helm and Helm Charts</h2>

Helm and Helm Charts - Study Tips
For the KCNA exam a basic understanding of Helm as a package manager solution for Kubernetes is required.


Helm es una herramienta de gestión de paquetes para Kubernetes. Facilita la instalación, configuración y gestión de aplicaciones y servicios en clústeres de Kubernetes a través de charts (paquetes de Kubernetes preconfigurados). Al igual que apt en Debian/Ubuntu o yum en CentOS/RHEL para sistemas operativos, Helm proporciona una manera sencilla de empaquetar, distribuir y gestionar aplicaciones dentro de un clúster Kubernetes.

¿Qué es un "Helm Chart"?
Un Helm Chart es un conjunto de archivos que describen los recursos de Kubernetes necesarios para ejecutar una aplicación. Esto incluye:

Archivos YAML que definen Pods, Services, Deployments, ConfigMaps, Secrets, etc.
Plantillas configurables que permiten personalizar la instalación de la aplicación según las necesidades del entorno o del usuario.

![image](https://github.com/user-attachments/assets/505a0315-a701-413c-bfd7-09a7fd3af035)

Bonito...

Intalamos la dependencia de tree con el gestor brew, ya visualisamos en forma de arbol: 

![image](https://github.com/user-attachments/assets/9623d5a8-8061-43dc-a965-f293f2eabbf2)


<h4>Como estan compuestos los archivos </h4>

Como esta compuesto el archivo Chart.yaml

![image](https://github.com/user-attachments/assets/f23f1994-02be-42aa-8d24-63d4aebc97d1)

Como esta compuesto el archivo values.yaml (es solo una primera parte porque este archivo es extenso)

![image](https://github.com/user-attachments/assets/5f88c016-39dd-44a1-94e3-f150dc055fc9)


Desplegando una app con Helm

![image](https://github.com/user-attachments/assets/b92a4bbc-092e-4d0d-ac32-215a4401e80d)


Comands

- helm install <release-name> <chart> [flags] : instala un gráfico (chart) de Helm en un clúster de Kubernetes.

- helm list: para listar los "releases" (despliegues) de aplicaciones que han sido instalados en un clúster de Kubernetes mediante Helm.

- helm search <hub|repo> [term] [flags] : Busca gráficos (charts) en un repositorio de Helm.

- helm repo <command> [flags]; Gestiona los repositorios de Helm (agregar, actualizar, listar).



<h2>Questions</h2>

What is the primary function of Helm in Kubernetes?
- Monitoring Kubernetes nodes
- Simplifying the management of Kubernetes applications (Correct)
- Providing network security for Kubernetes clusters
- Automating the backup of Kubernetes data


Which of the following is required for Helm's plugin installation?
- Docker
- Python
- git (Correct)
- Node.js

Explanation: For installing Helm plugins, the required tool is git. Many Helm plugins are hosted in Git repositories, so git is needed to clone these repositories during the plugin installation process.

What is the purpose of Helm Charts in Kubernetes?
- To monitor resource usage
- To manage ingress controllers
- To facilitate deployment and management of applications (Correct)
- To encrypt sensitive data

How can Helm Charts be packaged for distribution?
- Using the helm distribute command
- With the docker package utility
- Using the helm package command (Correct)
- Through the kubectl package command

Explanation:

Explanation:
Helm Charts can be packaged for distribution using the helm package command. This command packages a chart into a .tgz file (a compressed tarball) that can be shared or uploaded to a Helm chart repository.

Here’s an example of how you would package a Helm chart: <code>helm package ./my-chart</code>


<h2>Service Mesh</h2>

Service Meshes - Study Tips
For the KCNA exam pay particular attention to the following -

The purpose of Service Meshes
The main components, Proxy and Data Plane
Common open source offerings for Service Meshes
The role of the SMI


Un service mesh, es una capa dentro de la infraestructura de una aplicación de microservicios que hace que la comunicación entre servicios sea flexible, confiable y rápida. Proporciona descubrimiento de servicios, equilibrio de carga, cifrado, autenticación y autorización, soporte para el patrón de interruptor de circuito (circuit-breaker) entre otras capacidades.

¿Porqué es necesario un Service Mesh?
En las arquitecturas monolíticas, tratamos casi exclusivamente con tráfico norte-sur, pero con microservicios, debemos tratar con el tráfico este-oeste, ya que con los monolitos, los diferentes componentes se comunican entre sí mediante llamadas dentro de la aplicación. Con microservicios, reemplazamos las llamadas dentro de la aplicación con comunicación entre APIs a través de la red. Esto significa que los diferentes servicios dentro de nuestra arquitectura no tienen por que saber el uno del otro, mientras cada API sea consumible.

El tráfico este-oeste (entre APIs de nuestros microservicios) representa una mayor desafío, este tráfico demandan más en términos de estandarización de llamadas entre cada microservicio, su monitorización, el despliegue y aprovisionamiento de recursos.


![image](https://github.com/user-attachments/assets/c8488035-1857-4f62-8f21-886aaf5b95c8)

![image](https://github.com/user-attachments/assets/293b0ced-868b-4287-bb21-60e689903145)

![image](https://github.com/user-attachments/assets/3ce7b310-6c65-4e73-8603-9186215fa326)



Componentes de Un Service Mesh

![image](https://github.com/user-attachments/assets/480d6cec-0914-475f-9ed0-c5da89fe0b0d)


Data Plane
The data plane handles the actual traffic between services. It comprises a collection of intelligent proxies, deployed as sidecars alongside service instances. These proxies intercept and manage all network communication between microservices. They apply various policies such as routing, load balancing, and authentication, ensuring that data packets reach their intended destinations.

The proxies within the data plane are responsible for executing detailed instructions provided by the control plane. They perform tasks like encrypting and decrypting requests for secure transmission, implementing rate limiting to prevent service overload, and recording telemetry data for monitoring purposes.

The Control Plane
The control plane acts as the brain of the service mesh architecture, orchestrating the configuration and management of the network’s communication rules. It centralizes policy decisions and distributes these policies to the data plane’s proxies for enforcement. This enables dynamic updates and communication management without direct code changes or redeployments.

The control plane provides a unified interface for administrators to define, apply, and monitor policies across all services. Through this interface, operators can implement security measures like authentication and authorization, manage traffic flow via routing rules, and observe system behavior through logging and monitoring tools.




***Importante***, conocer que es SMI (Service Mesh Interface)

Service Mesh Interface provides:
- A standard interface for service meshes on Kubernetes
- A basic feature set for the most common service mesh use cases
- Flexibility to support new service mesh capabilities over time
- Space for the ecosystem to innovate with service mesh technology


What SMI covers
Service Mesh Interface is a specification that covers the most common service mesh capabilities:

- Traffic policy – apply policies like identity and transport encryption across services
- Traffic telemetry – capture key metrics like error rate and latency between services
- Traffic management – shift traffic between different services
 
Kubernetes Native
The SMI is specified as a collection of Kubernetes Custom Resource Definitions (CRD) and Extension API Servers. These APIs can be installed onto any Kubernetes cluster and manipulated using standard tools.


Tambien es importante conocer que es Istio

Istio extends Kubernetes to establish a programmable, application-aware network. Working with both Kubernetes and traditional workloads, Istio brings standard, universal traffic management, telemetry, and security to complex deployments.

Select the features you want and Istio deploys proxy infrastructure as needed. Use the zero-trust tunnel for Layer 4 performance and security, or add the powerful Envoy service proxy for Layer 7 features.


Istio es una plataforma de código abierto diseñada para facilitar la gestión de microservicios. Se usa principalmente en entornos de Kubernetes, aunque también se puede usar en otras infraestructuras. Su objetivo principal es ofrecer soluciones para la conectividad, seguridad, observabilidad y gestión del tráfico entre los microservicios dentro de una arquitectura distribuida.

Funciones principales de Istio:
Gestión del Tráfico: Istio permite controlar cómo se enrutan las solicitudes entre los microservicios, proporcionando funcionalidades como:

Balanceo de carga.
Enrutamiento avanzado (por ejemplo, canary deployments, A/B testing).
Control de tráfico basado en condiciones, como la versión del servicio o la carga.
Seguridad: Istio proporciona una capa de seguridad para las comunicaciones entre servicios mediante:

Autenticación y autorización: Puede garantizar que las comunicaciones entre microservicios sean seguras, utilizando mTLS (mutual TLS) para encriptar las comunicaciones y verificar las identidades de los servicios.
Control de acceso: Permite definir políticas que limitan quién puede acceder a qué servicios.
Observabilidad: Ayuda a obtener visibilidad completa del comportamiento de los microservicios, proporcionando métricas, logs y trazas a través de:

Recopilación de métricas: Istio integra herramientas como Prometheus para el monitoreo de métricas de tráfico.
Trazabilidad distribuida: Gracias a herramientas como Jaeger o Zipkin, Istio permite rastrear la trayectoria de las solicitudes a través de todos los servicios involucrados en un proceso.
Política y Gobernanza: Permite definir políticas a nivel de red para gestionar el comportamiento de los servicios, como la limitación de tasas, la gestión de errores, etc.

Componentes de Istio:
Envoy: Es un proxy de red de alto rendimiento que Istio utiliza para interceptar el tráfico entre los microservicios. Cada microservicio se comunica a través de un proxy Envoy, lo que permite a Istio aplicar políticas y recopilar datos sin necesidad de modificar el código de los servicios.
Istiod: Es el componente de control de Istio, que gestiona la configuración y las políticas, y coordina la comunicación entre los proxies Envoy.
Ventajas de Istio:
Desacopla la lógica de red y seguridad del código de los microservicios: Los desarrolladores no necesitan implementar funcionalidades de red y seguridad en cada microservicio individualmente.
Fácil integración con herramientas de monitoreo y trazabilidad.
Escalabilidad y flexibilidad en el enrutamiento y control del tráfico.

Example of a Service Mesh: Istio Architecture Diagram
Istio is a popular, open source service mesh solution. The following diagram shows the architecture of the Istio service mesh.

![image](https://github.com/user-attachments/assets/28c89c33-aec8-4306-ada9-784f2241ebe3)






Leer Este articulo, muy bueno: https://medium.com/nerd-for-tech/microservice-design-pattern-sidecar-sidekick-pattern-dbcea9bed783


Sidecar Pattern

Deploy components of an application into a separate process or container to provide isolation and encapsulation. This pattern can also enable applications to be composed of heterogeneous components and technologies.

This pattern is named Sidecar because it resembles a sidecar attached to a motorcycle. In the pattern, the sidecar is attached to a parent application and provides supporting features for the application. The sidecar also shares the same lifecycle as the parent application, being created and retired alongside the parent. The sidecar pattern is sometimes referred to as the sidekick pattern and is a decomposition pattern.

Sidecar Pattern in k8s

The first single-node pattern is the sidecar pattern. The sidecar pattern is a single-node pattern made up of two containers. The first is the application container. It contains the core logic for the application. Without this container, the application would not exist. In addition to the application container, there is a sidecar container. The role of the sidecar is to augment and improve the application container, often without the application container’s knowledge. In its simplest form, a sidecar container can be used to add functionality to a container that might otherwise be difficult to improve. Sidecar containers are coscheduled onto the same machine via an atomic container group, such as the pod API object in Kubernetes. In addition to being scheduled on the same machine, the application container and sidecar container share a number of resources, including parts of the filesystem, hostname and network, and many other namespaces. A generic image of this sidecar pattern is shown in Figure 2-1.

![image](https://github.com/user-attachments/assets/b95f5c96-f9fb-4463-93d5-207671867974)


Context and problem
Applications and services often require related functionality, such as monitoring, logging, configuration, and networking services. These peripheral tasks can be implemented as separate components or services.

If they're tightly integrated into the application, they can run in the same process as the application, making efficient use of shared resources. However, this also means they're not well isolated, and an outage in one of these components can affect other components or the entire application. Also, they usually need to be implemented using the same language as the parent application. As a result, the component and the application have close interdependence on each other.

If the application is decomposed into services, then each service can be built using different languages and technologies. While this gives more flexibility, it means that each component has its own dependencies and requires language-specific libraries to access the underlying platform and any resources shared with the parent application. In addition, deploying these features as separate services can add latency to the application. Managing the code and dependencies for these language-specific interfaces can also add considerable complexity, especially for hosting, deployment, and management.

Solution
Co-locate a cohesive set of tasks with the primary application, but place them inside their own process or container, providing a homogeneous interface for platform services across languages.

Diagram of the Sidecar pattern

A sidecar service isn't necessarily part of the application, but is connected to it. It goes wherever the parent application goes. Sidecars are supporting processes or services that are deployed with the primary application. On a motorcycle, the sidecar is attached to one motorcycle, and each motorcycle can have its own sidecar. In the same way, a sidecar service shares the fate of its parent application. For each instance of the application, an instance of the sidecar is deployed and hosted alongside it.

Advantages of using a sidecar pattern include:

A sidecar is independent from its primary application in terms of runtime environment and programming language, so you don't need to develop one sidecar per language.

The sidecar can access the same resources as the primary application. For example, a sidecar can monitor system resources used by both the sidecar and the primary application.

Because of its proximity to the primary application, there's no significant latency when communicating between them.

Even for applications that don't provide an extensibility mechanism, you can use a sidecar to extend functionality by attaching it as its own process in the same host or sub-container as the primary application.

The sidecar pattern is often used with containers and referred to as a sidecar container or sidekick container.


Al Español

El Sidecar Pattern (o patrón sidecar) es un patrón arquitectónico comúnmente utilizado en arquitecturas de microservicios, particularmente cuando se trabaja con contenedores, como en entornos de Kubernetes. En este patrón, una aplicación principal (o servicio) se despliega junto a un contenedor o proceso adicional que ofrece funcionalidades complementarias, pero que no forma parte directa de la lógica de negocio de la aplicación principal.

Este contenedor adicional se conoce como el sidecar, y generalmente se utiliza para gestionar aspectos relacionados con la infraestructura, la observabilidad, la seguridad, el monitoreo, o la gestión del tráfico sin modificar el código de la aplicación principal.

Características del Sidecar Pattern:
Desacoplamiento: El sidecar opera de manera independiente del servicio principal, lo que permite que la aplicación principal se enfoque en su lógica de negocio, mientras que el sidecar gestiona tareas transversales o de infraestructura.

Cohabitación: El sidecar y el servicio principal comparten el mismo ciclo de vida y el mismo entorno de ejecución (como un pod en Kubernetes), pero operan de forma autónoma en cuanto a sus responsabilidades y funciones.

Transparencia: El sidecar generalmente se implementa sin que el código del servicio principal tenga que cambiar. Esto permite añadir funcionalidades adicionales de manera transparente.





Concepto de Sidecar containers

Sidecar containers are the secondary containers that run along with the main application container within the same Pod. These containers are used to enhance or to extend the functionality of the primary app container by providing additional services, or functionality such as logging, monitoring, security, or data synchronization, without directly altering the primary application code.

Typically, you only have one app container in a Pod. For example, if you have a web application that requires a local webserver, the local webserver is a sidecar and the web application itself is the app container.

Sidecar containers in Kubernetes
Kubernetes implements sidecar containers as a special case of init containers; sidecar containers remain running after Pod startup. This document uses the term regular init containers to clearly refer to containers that only run during Pod startup.

Provided that your cluster has the SidecarContainers feature gate enabled (the feature is active by default since Kubernetes v1.29), you can specify a restartPolicy for containers listed in a Pod's initContainers field. These restartable sidecar containers are independent from other init containers and from the main application container(s) within the same pod. These can be started, stopped, or restarted without effecting the main application container and other init containers.

You can also run a Pod with multiple containers that are not marked as init or sidecar containers. This is appropriate if the containers within the Pod are required for the Pod to work overall, but you don't need to control which containers start or stop first. You could also do this if you need to support older versions of Kubernetes that don't support a container-level restartPolicy field.




Questions

What are the two main components of a Service Mesh?
- Data Plane and Application Plane
- Data Plane and Control Plane (Correct)
- Control Plane and Configuration Plane
- Communication Plane and Data Plane


What pattern is commonly used in the Data Plane of a Service Mesh?
- Monolithic pattern
- Sidecar pattern (Correct)
- Singleton pattern
- Observer pattern


What is one of the key security features provided by a Service Mesh?
- Basic HTTPS encryption
- Mutual TLS  (Correct)
- Simple password authentication
- API key validation

Explanation

The correct answer is: Mutual TLS (mTLS)

One of the key security features provided by a service mesh is mutual TLS (mTLS), which ensures that both the client and the server authenticate each other during communication. This feature encrypts the traffic between services and verifies the identity of both parties, significantly enhancing security in microservices architectures.

Concepto adicional: mutual TLS

What is mutual TLS (mTLS)?
Mutual TLS, or mTLS for short, is a method for mutual authentication. mTLS ensures that the parties at each end of a network connection are who they claim to be by verifying that they both have the correct private key. The information within their respective TLS certificates provides additional verification.

mTLS is often used in a Zero Trust security framework* to verify users, devices, and servers within an organization. It can also help keep APIs secure<.


What is TLS?
Transport Layer Security (TLS) is an encryption protocol in wide use on the Internet. TLS, which was formerly called SSL, authenticates the server in a client-server connection and encrypts communications between client and server so that external parties cannot spy on the communications. There are three important things to understand about how TLS works:


What does SMI stand for in the context of Service Meshes?
- Service Mesh Integration
- Service Mesh Interface (Correct)  (este concepto ya lo vimos)
- Service Management Interface
- Service Mesh Infrastructure


What is the primary goal of the Service Mesh Interface (SMI)?
- To provide a specific implementation for Service Meshes
- To create a unified programming language for Service Meshes
- To offer a common, interoperable interface for various Service Mesh solutions  (Correct)
- To replace Kubernetes in cloud-native environments


The correct answer is:

To offer a common, interoperable interface for various Service Mesh solutions

Explanation:
The Service Mesh Interface (SMI) is a set of standards and specifications aimed at providing a common, interoperable API for service mesh solutions. Its primary goal is to create a way for different service mesh technologies (like Istio, Linkerd, Consul, etc.) to work together with a consistent set of APIs. This helps developers and operators to work with service meshes in a more unified manner, without being tied to a specific implementation.

Here’s why the other options are incorrect:

To provide a specific implementation for Service Meshes: This is not the goal of the SMI. Instead of offering a specific implementation, the SMI aims to standardize the interfaces and APIs so that different service meshes can comply with the same set of standards.

To create a unified programming language for Service Meshes: The SMI does not focus on creating a new programming language. Its goal is to standardize APIs and interfaces, not to change how developers write code for service meshes.
To replace Kubernetes in cloud-native environments: Kubernetes is a container orchestration platform, and the SMI has no intention of replacing Kubernetes. The SMI works alongside Kubernetes in cloud-native environments, specifically focusing on the network layer (service-to-service communication) provided by service meshes.


Which aspect is NOT directly addressed by Service Mesh Interface (SMI) API specifications?
- Traffic management
- Access control 
- Metrics
- Data storage (Correct)

Explanation:

The correct answer is:

Data storage

Explanation:
The Service Mesh Interface (SMI) focuses on standardizing several aspects of service mesh functionality, particularly around the management of microservices in cloud-native environments. However, data storage is not one of the aspects addressed by the SMI.

Here’s a breakdown of the other options:

- Traffic management: SMI provides specifications for managing traffic between services, such as routing, load balancing, and policy enforcement (e.g., retries, timeouts). This is directly addressed by SMI.

- Access control: SMI includes specifications for managing access control, such as defining policies for which services can communicate with each other, enforcing mutual TLS, and other security controls. This is an important aspect of service meshes and is included in the SMI API.

- Metrics: The SMI also deals with the collection and exposure of metrics to allow monitoring and observability. It provides a standard interface for gathering metrics related to service mesh behavior (e.g., traffic volume, latencies, errors).


In the context of Service Meshes, what is the role of the Control Plane?
- Manages database interactions
- Acts as a client application
- Serves as a management hub, configuring and directing proxies (Correct)
- Directly handles user requests



<h2>Observability</h2>


Cloud Native Observability - Study Tips
For the KCNA exam you will need an understanding of the following -

The 3 pillars of Cloud Native Observability
Where and why you would use each Pillar, i.e. Logs, Metrics, Traces
The different types of Metrics, i.e. Gauges, Counters, Meters, Histograms
The relation between Alerting and the 3 pillars of Cloud Native Observability
Be aware of kubectl top
Have an understanding of options such as OpenTracing/OpenTelemetry and that these operate at the Application layer



CLoud Native Observability

![image](https://github.com/user-attachments/assets/5737b6a6-cc56-4e5d-804e-1af8d25d150d)

Definitions

<h3>Logs</h3>

- Logs are available in a variety of formats 
- Typically the verbosity level can be adjusted 
- Often file based but other options like streaming exist 
- Can sometimes be manipulated through the likes of syslog;



<h3>Metrics</h3>

- Emitted over a period of time
- Memory Metrics — Amount of Memory used
- Typically time based and are measured at set intervals
- Useful insight for reviewing whether a component is as expected, underperforming or overperforming


![image](https://github.com/user-attachments/assets/648e6021-1a8f-49dd-9b65-813f02d9bbaa)


- Gauges: los Gauges son un tipo de métrica que mide un valor que puede cambiar hacia arriba o hacia abajo en cualquier momento. A diferencia de los contadores (counters), que solo incrementan, los gauges pueden reflejar valores dinámicos y fluctuantes a lo largo del tiempo, lo que los hace útiles para monitorear métricas que pueden aumentar o disminuir, como el uso de memoria, la temperatura de un sistema o el número de elementos en una cola.

Características principales de los Gauges:
Valores dinámicos: Pueden representar valores que suben y bajan, como el uso de CPU, el tamaño de la memoria utilizada, la cantidad de conexiones abiertas, etc.

Instantáneas: Miden el valor en un punto específico del tiempo. No se suman ni se agregan como un contador, sino que reflejan el estado actual de la métrica.

Ejemplos comunes:

Uso de memoria o almacenamiento.
Número de conexiones activas en un servidor.
Número de usuarios actualmente conectados.
Temperatura de un dispositivo o servidor.
Posibles valores: Pueden tomar cualquier valor dentro de un rango permitido, como un número entero o un valor decimal.

![image](https://github.com/user-attachments/assets/74fc4973-93fe-4dcc-b657-75c5b071f972)


- Contadores (Counters): SOLO aumentan, NUNCA disminuyen. Por ejemplo, un contador podría ser el número de solicitudes HTTP recibidas (de unas API Request).

 ![image](https://github.com/user-attachments/assets/1bb90103-4006-4285-94b6-a77c3af8657a)


 - Meters

El término meter (o métrica de tasa en algunos casos) se refiere a un tipo de métrica que mide la frecuencia con la que ocurren ciertos eventos en un sistema durante un período de tiempo determinado. Es muy similar a un counter, pero con un enfoque en la tasa de ocurrencia de los eventos en lugar de solo contar su número total.

Características principales de un Meter:
Medición de la tasa de eventos: Un meter no solo cuenta los eventos, sino que también mide cuántos eventos ocurren por unidad de tiempo (por ejemplo, eventos por segundo, por minuto, etc.). Esto es útil cuando se quiere saber qué tan rápido está ocurriendo un proceso o acción.

Frecuencia o tasa: Un meter se utiliza para calcular la frecuencia o tasa de eventos. Ejemplos incluyen cuántas solicitudes HTTP por segundo o cuántos mensajes por minuto están siendo procesados en un sistema.

Conceptos clave:

Eventos contados: Similar a un contador, un meter puede contar eventos, pero lo hace con el enfoque adicional de la tasa con la que ocurren.
Promedio de tasas: Calcula promedios de eventos por unidad de tiempo. Por ejemplo, puede calcular la tasa de peticiones HTTP que llegan a un servidor.
Tasa instantánea: Mide la tasa de eventos en un intervalo muy corto de tiempo (por ejemplo, cuántos eventos están ocurriendo en el último segundo).
Acumulación de eventos: A lo largo del tiempo, los eventos se acumulan, y el meter puede ofrecer estadísticas como:

Total de eventos contados (similar a un contador).
Promedio de eventos por segundo, minuto, hora, etc.
La tasa instantánea de eventos.
Ejemplos comunes de Meters:
Solicitudes HTTP por segundo: Un meter podría medir cuántas solicitudes HTTP se reciben por segundo en un servidor web.

Métrica: Número de solicitudes por segundo (requests per second, RPS).
Errores por minuto: Un meter podría medir cuántos errores HTTP 500 se producen por minuto.

Métrica: Errores 500 por minuto.
Tasa de eventos de una cola: Si tienes un sistema de procesamiento de eventos o tareas, un meter podría medir cuántos eventos o tareas se procesan por minuto.

Métrica: Número de tareas procesadas por segundo o minuto.
Tasa de consumo de mensajes en un sistema de mensajería: En sistemas que consumen y procesan mensajes (por ejemplo, Kafka, RabbitMQ), un meter podría medir la tasa a la que los mensajes son consumidos o procesados.

Diferencias con otros tipos de métricas:
Counters: Los contadores simplemente cuentan el número total de eventos que han ocurrido hasta el momento. En cambio, un meter mide la frecuencia con la que ocurren esos eventos a lo largo del tiempo.

Ejemplo de contador: número total de solicitudes HTTP.
Ejemplo de meter: tasa de solicitudes HTTP por segundo.
Gauges: Los gauges son métricas que pueden aumentar o disminuir (por ejemplo, el uso de memoria o el número de conexiones abiertas). Los meters, en cambio, se centran en la tasa de eventos durante un periodo de tiempo.

Histograms: Los histogramas miden la distribución de los valores de ciertos eventos, como las latencias. Los meters miden las tasas de esos eventos, pero no sus distribuciones.




<h3>Histograms</h3>

A histogram is a graphical representation of the distribution of numerical data. It's essentially a bar chart, where each bar represents a range of values, and the height of the bar corresponds to the frequency of data points within that range.

For example, if you have a dataset of response times for a web application, a histogram can show you how many requests fall into different time intervals, such as 0-100ms, 100-200ms, and so on.

Histograms are useful in observability because they enable you to quickly understand the shape of the data and identify patterns or anomalies. A histogram of number of errors can quickly show you that errors spiked at a specific time and how the number of errors recovered after that.

![image](https://github.com/user-attachments/assets/c4968203-9257-468c-9423-6b4d61e35705)




<h3>Traces</h3>

Son un mecanismo para seguir el flujo de una solicitud o evento a través de los diferentes componentes de un sistema distribuido. Las trazas permiten identificar cómo una solicitud interactúa con los distintos servicios, aplicaciones o microservicios que componen el sistema, proporcionando una visión detallada de la latencia, los cuellos de botella y el comportamiento de las interacciones entre sistemas.

- An essential component in Cloud Native Observablity
- Trace/Track progress of request as it traverses through the system
- Provides fantastic insights!
- End to End lifecycle


![image](https://github.com/user-attachments/assets/5fae7a5e-123e-4e94-9334-1ad32e34b451)





Observability and Monitoring

![image](https://github.com/user-attachments/assets/2a63f46b-3963-403b-bae3-8709d787ef99)




<h3>Self Monitoring</h3>

Self-monitoring observability is a software practice that involves observability stacks monitoring each other to reduce the risk of unexpected outages. It can be used in addition to redundancy and high availability to help prevent correlated failures

Self-monitoring (autovigilancia o monitoreo autónomo) es el proceso mediante el cual un sistema o aplicación monitorea su propio estado, rendimiento y salud sin intervención humana directa. En lugar de depender exclusivamente de herramientas externas o equipos de monitoreo para detectar problemas o anomalías, un sistema de self-monitoring se integra con métricas y mecanismos internos que le permiten autoevaluarse y, en algunos casos, tomar medidas automáticas en respuesta a eventos o condiciones detectadas.


Proyectos de Observability

![image](https://github.com/user-attachments/assets/619cd3b4-5bd4-4e1b-9153-0c59f7f2e80b)




Introduction
Purpose: Aims to provide a standardised and easy way to trace requests across distributed systems, helping developers to monitor and troubleshoot complex microservices architectures.
Vendor-Neutral API: It offers a way to collect trace data without being tied to any specific tracing backend (like Jaeger or Zipkin). This flexibility allows for easy integration and migration between different tracing systems.


How OpenTracing/OpenTelemetry Operates at the Application Layer

- Instrumentation: Developers add code to their applications to create and manage spans. These spans represent individual operations or requests, capturing essential data such as start and end times, tags, and logs.

- Span Context Propagation: As requests move through different services and processes, the span context is propagated, ensuring a continuous trace across service boundaries. This is often handled via HTTP headers or messaging metadata.

- Data Reporting: The instrumented applications report span data to a tracing backend. This data collection is designed to be low-overhead to minimize the impact on application performance.

- Analysis and Visualisation: The backend (like Jaeger or Zipkin) aggregates this data, providing a visual representation of the traces. This visualisation aids in performance analysis, debugging, and optimisation.


Resources for Further Learning

- Official Documentation: OpenTracing Website (the project is recently archived but still has valuable information) provides guides, API documentation, and a conceptual overview of distributed tracing: https://opentracing.io/
- OpenTelemetry Documentation: OpenTelemetry provides guides on moving from OpenTracing to OpenTelemetry: https://opentelemetry.io/docs/migration/opentracing/
- By integrating OpenTracing/OpenTelemetry into applications, developers gain critical insights into the performance and behaviour of their systems, making it easier to identify and solve issues in a distributed environment.




Proyectos de Observabilidad en la CNCF

OpenTracing

OpenTracing es un proyecto que define una API abierta y neutral para rastrear y monitorear solicitudes de aplicaciones: 
Permite a los desarrolladores recopilar datos sobre el rendimiento de las aplicaciones distribuidas 
Permite a los usuarios evitar el bloqueo de proveedores al permitir cambiar el implementador de OpenTracing 
Permite a los desarrolladores de marcos de trabajo y bibliotecas compartidas proporcionar una funcionalidad de rastreo lista para usarse 

OpenTracing permite: 
Identificar cuellos de botella y problemas de latencia
Diagnosticar fallas
Comprender la secuencia de eventos, dependencias, y paths dentro del sistema
Facilitar la localización de cuellos de botella de rendimiento
Hacer más fácil la resolución de problemas de errores
Proporcionar información sobre el comportamiento de la aplicación


Opentelemetry

Tambien fue creado en la CNCF. OpenTelemetry is a collection of APIs, SDKs, and tools. Use it to instrument, generate, collect, and export telemetry data (metrics, logs, and traces) to help you analyze your software’s performance and behavior.
![image](https://github.com/user-attachments/assets/1d735403-aac3-4e32-97cd-bbd5123c2d85)


El comando kubectl top (Entender)

Shows the current resource utilization for nodes or pods

Explanation:
The kubectl top command is used in Kubernetes to display resource usage metrics for nodes or pods in the cluster, such as CPU and memory utilization. It provides real-time data about how much CPU and memory each resource (node or pod) is consuming, which helps in monitoring the health and performance of your Kubernetes cluster.

For example:

kubectl top nodes: Shows the resource usage (CPU, memory) for all nodes in the cluster.
kubectl top pods: Displays the resource usage (CPU, memory) for all pods running in the cluster.
This command relies on the Metrics Server, a component that collects resource usage data and makes it available to tools like kubectl.




Questions

What is the primary purpose of Observability in Cloud Native systems?
- To manage user permissions and access
- To accurately measure a system's state through its output (Correct)
- To enhance the graphical user interface of the system
- To increase the storage capacity of cloud services


Which of the following is not a type of telemetry in the context of Cloud Native Observability?
- Logs
- Metrics 
- Traces
- Encryption (Correct)


In Cloud Native Observability, what are Logs primarily used for?
- To measure the network bandwidth
- To encrypt sensitive data
- To output messages from programs, applications, and processes (Correct)
- To track the physical location of devices


What characteristic of Metrics makes them essential for Observability?
- They are static and unchangeable
- They are cumulative and always increase
- They are time-based and measured at set intervals (Correct)
- They provide real-time user feedback

Explanation:

The correct answer is: - They are time-based and measured at set intervals

Metrics are essential for observability because they provide a quantitative view of a system's behavior over time. By being time-based and measured at regular intervals, metrics allow you to track changes, trends, and performance in your system. This time-based data is crucial for understanding how the system behaves, identifying issues, and making informed decisions on improvements.


What is a Counter in the context of Cloud Native Observability?
- A device that measures physical properties
- A cumulative metric that increases over time (Correct)
- A statistical method for data encryption 
- A tool for visualizing network topology



Which of these is an example of a Trace in Cloud Native Observability?
- A static record of a user's login history
- Tracking the process of a request through a system (Correct)
- A snapshot of current server capacity
- A log file stored on a physical disk


What role do Alerts play in Cloud Native Observability?
- They predict future system states based on historical data
- They provide notifications about system anomalies or issues (Correct)
- They serve as a primary storage method for telemetry data
- They act as a backup system for logs, metrics, and trace


What are the three fundamental pillars of Cloud Native Observability?
- Encryption, Compression, and Redundancy
- Logs, Metrics, and Traces             <-  (Correct)
- Authentication, Authorization, and Accounting
- Bandwidth, Latency, and Throughput


Which pillar of Cloud Native Observability would be most useful for predicting future resource usage?
- Logs
- Metrics  (Correct)
- Traces
- Alerts


In Cloud Native Observability, which format would be considered user-friendly for outputting logging data whilst supporting complex and hierarchical data?
- CSV
- JSON (Correct)
- YAML
- HTML

The correct answer is:

JSON

Explanation:
In Cloud Native Observability, JSON (JavaScript Object Notation) is widely considered the most user-friendly and flexible format for outputting logging data, especially when dealing with complex and hierarchical data. Here’s why:

Hierarchical Structure: JSON supports nested structures (objects and arrays), making it ideal for representing complex and hierarchical data. This allows logs to contain multiple levels of information, such as timestamps, log levels, metadata, and context in a structured way.

Machine Readable: JSON is easy to parse by both humans and machines. It’s commonly used for integration with log aggregators, monitoring tools, and centralized logging systems like Elasticsearch, Prometheus, Splunk, and others.

Interoperability: JSON is a widely accepted and standardized format, supported by most programming languages and observability platforms. This ensures compatibility with various tools, dashboards, and automation systems.




In which layer of a software system do OpenTracing and OpenTelemetry primarily operate?
- Network
- Operating System
- Application (Correct)
- Hardware



The correct answer is:

- Application

Explanation:
OpenTracing and OpenTelemetry primarily operate at the Application layer of a software system. They are frameworks for distributed tracing and observability, designed to provide insights into how requests and transactions flow through various services, applications, and components in a distributed system.

OpenTracing: It provides a standard API for tracing requests and measuring their latency across multiple services or microservices.
OpenTelemetry: It is a more comprehensive and modern framework that combines tracing, metrics, and logs. OpenTelemetry standardizes the collection and transmission of observability data from applications, services, and infrastructure.




What does the kubectl top command do in a Kubernetes environment?

- Lists the most frequently used Kubernetes commands
- Shows the current resource utilization for nodes or pods (Correct)
- Displays the top layer of the Kubernetes architecture 
- Ranks the services in the cluster based on traffic



The correct answer is:

- Shows the current resource utilization for nodes or pods

Explanation:
The kubectl top command is used in Kubernetes to display resource usage metrics for nodes or pods in the cluster, such as CPU and memory utilization. It provides real-time data about how much CPU and memory each resource (node or pod) is consuming, which helps in monitoring the health and performance of your Kubernetes cluster.

For example:

kubectl top nodes: Shows the resource usage (CPU, memory) for all nodes in the cluster.
kubectl top pods: Displays the resource usage (CPU, memory) for all pods running in the cluster.
This command relies on the Metrics Server, a component that collects resource usage data and makes it available to tools like kubectl.



LDAP and OIDC in k8s

- https://pmvk.medium.com/step-by-step-guide-to-integrate-ldap-with-kubernetes-1f3fe1ec644e
- https://medium.com/@extio/kubernetes-authentication-with-oidc-simplifying-identity-management-c56ede8f2dec



<h2>Taints and Tolerations</h2>


Node affinity is a property of Pods that attracts them to a set of nodes (either as a preference or a hard requirement). Taints are the opposite -- they allow a node to repel a set of pods.

Tolerations are applied to pods. Tolerations allow the scheduler to schedule pods with matching taints. Tolerations allow scheduling but don't guarantee scheduling: the scheduler also evaluates other parameters as part of its function.

Taints and tolerations work together to ensure that pods are not scheduled onto inappropriate nodes. One or more taints are applied to a node; this marks that the node should not accept any pods that do not tolerate the taints.

Concepts
You add a taint to a node using kubectl taint. For example,

kubectl taint nodes node1 key1=value1:NoSchedule
places a taint on node node1. The taint has key key1, value value1, and taint effect NoSchedule. This means that no pod will be able to schedule onto node1 unless it has a matching toleration.

To remove the taint added by the command above, you can run:

kubectl taint nodes node1 key1=value1:NoSchedule-
You specify a toleration for a pod in the PodSpec. Both of the following tolerations "match" the taint created by the kubectl taint line above, and thus a pod with either toleration would be able to schedule onto node1:

tolerations:
- key: "key1"
  operator: "Equal"
  value: "value1"
  effect: "NoSchedule"
tolerations:
- key: "key1"
  operator: "Exists"
  effect: "NoSchedule"
The default Kubernetes scheduler takes taints and tolerations into account when selecting a node to run a particular Pod. However, if you manually specify the .spec.nodeName for a Pod, that action bypasses the scheduler; the Pod is then bound onto the node where you assigned it, even if there are NoSchedule taints on that node that you selected. If this happens and the node also has a NoExecute taint set, the kubelet will eject the Pod unless there is an appropriate tolerance set.

Here's an example of a pod that has some tolerations defined:

pods/pod-with-toleration.yaml Copy pods/pod-with-toleration.yaml to clipboard
apiVersion: v1
kind: Pod
metadata:
  name: nginx
  labels:
    env: test
spec:
  containers:
  - name: nginx
    image: nginx
    imagePullPolicy: IfNotPresent
  tolerations:
  - key: "example-key"
    operator: "Exists"
    effect: "NoSchedule"
The default value for operator is Equal.

A toleration "matches" a taint if the keys are the same and the effects are the same, and:

the operator is Exists (in which case no value should be specified), or
the operator is Equal and the values should be equal.
Note:
There are two special cases:

If the key is empty, then the operator must be Exists, which matches all keys and values. Note that the effect still needs to be matched at the same time.

An empty effect matches all effects with key key1.

The above example used the effect of NoSchedule. Alternatively, you can use the effect of PreferNoSchedule.

The allowed values for the effect field are:

NoExecute
This affects pods that are already running on the node as follows:
Pods that do not tolerate the taint are evicted immediately
Pods that tolerate the taint without specifying tolerationSeconds in their toleration specification remain bound forever
Pods that tolerate the taint with a specified tolerationSeconds remain bound for the specified amount of time. After that time elapses, the node lifecycle controller evicts the Pods from the node.
NoSchedule
No new Pods will be scheduled on the tainted node unless they have a matching toleration. Pods currently running on the node are not evicted.
PreferNoSchedule
PreferNoSchedule is a "preference" or "soft" version of NoSchedule. The control plane will try to avoid placing a Pod that does not tolerate the taint on the node, but it is not guaranteed.
You can put multiple taints on the same node and multiple tolerations on the same pod. The way Kubernetes processes multiple taints and tolerations is like a filter: start with all of a node's taints, then ignore the ones for which the pod has a matching toleration; the remaining un-ignored taints have the indicated effects on the pod. In particular,

if there is at least one un-ignored taint with effect NoSchedule then Kubernetes will not schedule the pod onto that node
if there is no un-ignored taint with effect NoSchedule but there is at least one un-ignored taint with effect PreferNoSchedule then Kubernetes will try to not schedule the pod onto the node
if there is at least one un-ignored taint with effect NoExecute then the pod will be evicted from the node (if it is already running on the node), and will not be scheduled onto the node (if it is not yet running on the node).
For example, imagine you taint a node like this

kubectl taint nodes node1 key1=value1:NoSchedule
kubectl taint nodes node1 key1=value1:NoExecute
kubectl taint nodes node1 key2=value2:NoSchedule
And a pod has two tolerations:

tolerations:
- key: "key1"
  operator: "Equal"
  value: "value1"
  effect: "NoSchedule"
- key: "key1"
  operator: "Equal"
  value: "value1"
  effect: "NoExecute"
In this case, the pod will not be able to schedule onto the node, because there is no toleration matching the third taint. But it will be able to continue running if it is already running on the node when the taint is added, because the third taint is the only one of the three that is not tolerated by the pod.

Normally, if a taint with effect NoExecute is added to a node, then any pods that do not tolerate the taint will be evicted immediately, and pods that do tolerate the taint will never be evicted. However, a toleration with NoExecute effect can specify an optional tolerationSeconds field that dictates how long the pod will stay bound to the node after the taint is added. For example,

tolerations:
- key: "key1"
  operator: "Equal"
  value: "value1"
  effect: "NoExecute"
  tolerationSeconds: 3600
means that if this pod is running and a matching taint is added to the node, then the pod will stay bound to the node for 3600 seconds, and then be evicted. If the taint is removed before that time, the pod will not be evicted.

Example Use Cases
Taints and tolerations are a flexible way to steer pods away from nodes or evict pods that shouldn't be running. A few of the use cases are

Dedicated Nodes: If you want to dedicate a set of nodes for exclusive use by a particular set of users, you can add a taint to those nodes (say, kubectl taint nodes nodename dedicated=groupName:NoSchedule) and then add a corresponding toleration to their pods (this would be done most easily by writing a custom admission controller). The pods with the tolerations will then be allowed to use the tainted (dedicated) nodes as well as any other nodes in the cluster. If you want to dedicate the nodes to them and ensure they only use the dedicated nodes, then you should additionally add a label similar to the taint to the same set of nodes (e.g. dedicated=groupName), and the admission controller should additionally add a node affinity to require that the pods can only schedule onto nodes labeled with dedicated=groupName.

Nodes with Special Hardware: In a cluster where a small subset of nodes have specialized hardware (for example GPUs), it is desirable to keep pods that don't need the specialized hardware off of those nodes, thus leaving room for later-arriving pods that do need the specialized hardware. This can be done by tainting the nodes that have the specialized hardware (e.g. kubectl taint nodes nodename special=true:NoSchedule or kubectl taint nodes nodename special=true:PreferNoSchedule) and adding a corresponding toleration to pods that use the special hardware. As in the dedicated nodes use case, it is probably easiest to apply the tolerations using a custom admission controller. For example, it is recommended to use Extended Resources to represent the special hardware, taint your special hardware nodes with the extended resource name and run the ExtendedResourceToleration admission controller. Now, because the nodes are tainted, no pods without the toleration will schedule on them. But when you submit a pod that requests the extended resource, the ExtendedResourceToleration admission controller will automatically add the correct toleration to the pod and that pod will schedule on the special hardware nodes. This will make sure that these special hardware nodes are dedicated for pods requesting such hardware and you don't have to manually add tolerations to your pods.

Taint based Evictions: A per-pod-configurable eviction behavior when there are node problems, which is described in the next section.

Taint based Evictions
FEATURE STATE: Kubernetes v1.18 [stable]
The node controller automatically taints a Node when certain conditions are true. The following taints are built in:

node.kubernetes.io/not-ready: Node is not ready. This corresponds to the NodeCondition Ready being "False".
node.kubernetes.io/unreachable: Node is unreachable from the node controller. This corresponds to the NodeCondition Ready being "Unknown".
node.kubernetes.io/memory-pressure: Node has memory pressure.
node.kubernetes.io/disk-pressure: Node has disk pressure.
node.kubernetes.io/pid-pressure: Node has PID pressure.
node.kubernetes.io/network-unavailable: Node's network is unavailable.
node.kubernetes.io/unschedulable: Node is unschedulable.
node.cloudprovider.kubernetes.io/uninitialized: When the kubelet is started with an "external" cloud provider, this taint is set on a node to mark it as unusable. After a controller from the cloud-controller-manager initializes this node, the kubelet removes this taint.
In case a node is to be drained, the node controller or the kubelet adds relevant taints with NoExecute effect. This effect is added by default for the node.kubernetes.io/not-ready and node.kubernetes.io/unreachable taints. If the fault condition returns to normal, the kubelet or node controller can remove the relevant taint(s).

In some cases when the node is unreachable, the API server is unable to communicate with the kubelet on the node. The decision to delete the pods cannot be communicated to the kubelet until communication with the API server is re-established. In the meantime, the pods that are scheduled for deletion may continue to run on the partitioned node.

Note:
The control plane limits the rate of adding new taints to nodes. This rate limiting manages the number of evictions that are triggered when many nodes become unreachable at once (for example: if there is a network disruption).
You can specify tolerationSeconds for a Pod to define how long that Pod stays bound to a failing or unresponsive Node.

For example, you might want to keep an application with a lot of local state bound to node for a long time in the event of network partition, hoping that the partition will recover and thus the pod eviction can be avoided. The toleration you set for that Pod might look like:

tolerations:
- key: "node.kubernetes.io/unreachable"
  operator: "Exists"
  effect: "NoExecute"
  tolerationSeconds: 6000
Note:
Kubernetes automatically adds a toleration for node.kubernetes.io/not-ready and node.kubernetes.io/unreachable with tolerationSeconds=300, unless you, or a controller, set those tolerations explicitly.

These automatically-added tolerations mean that Pods remain bound to Nodes for 5 minutes after one of these problems is detected.

DaemonSet pods are created with NoExecute tolerations for the following taints with no tolerationSeconds:

node.kubernetes.io/unreachable
node.kubernetes.io/not-ready
This ensures that DaemonSet pods are never evicted due to these problems.

Taint Nodes by Condition
The control plane, using the node controller, automatically creates taints with a NoSchedule effect for node conditions.

The scheduler checks taints, not node conditions, when it makes scheduling decisions. This ensures that node conditions don't directly affect scheduling. For example, if the DiskPressure node condition is active, the control plane adds the node.kubernetes.io/disk-pressure taint and does not schedule new pods onto the affected node. If the MemoryPressure node condition is active, the control plane adds the node.kubernetes.io/memory-pressure taint.

You can ignore node conditions for newly created pods by adding the corresponding Pod tolerations. The control plane also adds the node.kubernetes.io/memory-pressure toleration on pods that have a QoS class other than BestEffort. This is because Kubernetes treats pods in the Guaranteed or Burstable QoS classes (even pods with no memory request set) as if they are able to cope with memory pressure, while new BestEffort pods are not scheduled onto the affected node.

The DaemonSet controller automatically adds the following NoSchedule tolerations to all daemons, to prevent DaemonSets from breaking.

node.kubernetes.io/memory-pressure
node.kubernetes.io/disk-pressure
node.kubernetes.io/pid-pressure (1.14 or later)
node.kubernetes.io/unschedulable (1.10 or later)
node.kubernetes.io/network-unavailable (host network only)
Adding these tolerations ensures backward compatibility. You can also add arbitrary tolerations to DaemonSets.


Como especificar y pasar a un namespace

- To avoid specifying the namespace with each kubectl command, you can define a Kubernetes context that includes the desired namespace. This allows you to set the context once and then use kubectl without specifying the namespace every time.


<h2>Versioning (Importante tenerlo en cuenta)</h2>

![image](https://github.com/user-attachments/assets/2bcd4d60-6830-44c4-8a74-f64d7aad68f7)

- When an API is updated to version 1 (v1), it is considered to be in the stable stage of development. At this stage, the API is considered to be mature, reliable, and ready for production use without major changes expected.
- The term "alpha" is used to refer to an early stage in the development of an API where it is still in the experimental phase and undergoing significant changes. APIs in the alpha stage are not stable and may have breaking changes.
- When an API is updated to version 1 (v1), it is considered to be in the stable stage of development. At this stage, the API is considered to be mature, reliable, and ready for production use without major changes expected.
- The term "production" is used to refer to the final stage in the development of an API where it is considered stable, reliable, and ready for use in a production environment. APIs in the production stage are expected to have minimal changes and be fully supported for users.


Overall explanation
Once an API is updated to version 1 (v1), it is typically referred to as reaching "stable" This stage signifies that the API has matured, and its core features and functionality have been stabilized, making it suitable for production use. Subsequent updates and enhancements to the API are expected to maintain backward compatibility with the v1 version, ensuring that existing applications and integrations continue to work without major disruptions.

https://kubernetes.io/docs/reference/using-api/



<h2>Spreed Contraints in kubernetes</h2>

Overall explanation
Spread constraints in Kubernetes are primarily used to evenly distribute pods of a particular service or application across the cluster's nodes, enhancing load balancing and resource utilization.

Incorrect Answers:

Spread constraints are not concerned with resource requests and limits but with pod distribution for load balancing.
never scheduling on the same node describes the purpose of anti-affinity rules, not spread constraints.
scheduling pods with specific labels don't he same node describes affinity rules for collocating pods, not spread constraints.

https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#pod-topology-spread-constraints




<h2>East-West Traffic</h2>

Overall explanation
In the context of service mesh, east-west traffic typically refers to communication between services within the data center or cluster. Service mesh solutions like Istio and Linkerd focus on managing and securing this internal service-to-service traffic.

In computer networking, east-west traffic is network traffic among devices within a specific data center. The other direction of traffic flow is north-south traffic, data flowing from or to a system physically residing outside the data center.

Traffic
As a result of virtualization, private cloud, converged, and hyper-converged infrastructure adoption, east-west traffic volumes have increased. Today many virtual functions including virtual firewalls, load balancers and other software-defined networking (SDN) perform various functions and services that previously ran on physical hardware. As these components relay data to each other, they increase traffic on the network, which can increase latency and cause network congestion.As disaggregated compute and storage becomes popular, east-west traffic volumes will increase.

https://en.wikipedia.org/wiki/East-west_traffic


Tráfico Este-Oeste (East-West Traffic) se refiere a la comunicación de datos que ocurre dentro de un centro de datos o un entorno de nube entre servicios, aplicaciones o componentes que forman parte de la misma red o sistema. Es decir, es tráfico que se mueve horizontalmente dentro de un clúster o entre servicios que se ejecutan en la misma región o zona de disponibilidad.

En contraste, el tráfico Norte-Sur (North-South) se refiere al tráfico que entra y sale de un centro de datos o de la nube (normalmente entre los usuarios finales y la aplicación o el sistema).


North - South Traffic

North-south traffic refers to network traffic that enters or exits an organization's internal network, as opposed to traffic that occurs within the network (referred to as "east-west" traffic). The terms "north-south" and "south-north" are used to describe the direction of traffic flow in relation to an organization's network perimeter.

North-south traffic typically refers to communication between devices inside an organization and devices or services outside of the organization, such as the internet or cloud-based services. This type of traffic often involves the exchange of sensitive information, such as user credentials, and is critical to the functioning of an organization's IT systems. Examples of north-south traffic include web browsing, email, and cloud-based applications.



<h2>Memory Default Namespaces</h2>


Overall explanation
If a namespace in Kubernetes has default limits of 1 CPU and 256Gi of memory, and a pod definition file within that namespace doesn't specify any resource requirements, then the default resources assigned to the pod would inherit from the namespace.

In this case, the pod would have the following default resource assignments:

CPU: 1 CPU core
Memory: 256Gi (gibibytes) of memory

These default values are inherited from the namespace's default limits. However, it's important to note that if the namespace's default limits are not explicitly set, Kubernetes will use its cluster-wide default settings or any defaults provided by the underlying infrastructure or Kubernetes distribution.

https://kubernetes.io/docs/tasks/administer-cluster/manage-resources/memory-default-namespace/



Leer

https://kubernetes.io/docs/tasks/administer-cluster/manage-resources/



<h2></h2>

Overall explanation
These agreements are often called "Service Level Agreements" (SLAs). A Service Level Agreement is a formal contract between a service provider (vendor) and a service consumer (user) that outlines the specific performance and reliability guarantees, including Service Level Objectives (SLOs), that the provider commits to delivering. SLAs help ensure transparency, define expectations, and establish accountability for the quality of the managed service.

Incorrect Answers:

all of these others are just acronyms that I made up :)

Leer ****importante***: https://www.atlassian.com/incident-management/kpis/sla-vs-slo-vs-sli

![image](https://github.com/user-attachments/assets/cb7831ea-08d0-4773-8ca5-fcea9bac202a)


<h2>Controllers and Reconciliation</h2>
Controllers are the core of Kubernetes, and of any operator.

It’s a controller’s job to ensure that, for any given object, the actual state of the world (both the cluster state, and potentially external state like running containers for Kubelet or loadbalancers for a cloud provider) matches the desired state in the object. Each controller focuses on one root Kind, but may interact with other Kinds.

We call this process reconciling.


What platform was the first to standardize the distribution of container images and comply with the OCI distribution specification?
The first platform to standardize the distribution of container images and comply with the OCI distribution specification was Docker. Docker's adoption of the OCI distribution specification contributed to greater compatibility and interoperability among container runtimes and tools in the containerization ecosystem. This move helped establish a common standard for storing, sharing, and distributing container images across various platforms.

Leer este articulo: https://www.docker.com/blog/donating-docker-distribution-to-the-cncf/



<h2>Scalability</h2>


Deploying a cloud-native application for effective autoscaling involves ensuring the application is designed to scale, creating an infrastructure that supports seamless resource expansion, and configuring autoscaling to meet user demand while also enabling cost-efficient downsizing during lower traffic periods.

Leer: https://glossary.cncf.io/scalability/



<h2>When scheduling a pod</h2>

When scheduling a pod in Kubernetes, several phases are used to determine the best node to place the pod. These phases include:

Filtering: In this phase, the scheduler filters out nodes that do not meet the pod's resource requirements, affinity/anti-affinity rules, and node selectors. Nodes that pass these filters move on to the next phase.

Scoring: Once the nodes have been filtered, the scheduler assigns a score to each node based on various factors, such as resource availability, load, and custom scheduling preferences (if specified). Nodes with higher scores are considered better candidates for placement.

Prioritization: After scoring, the scheduler prioritizes nodes based on the assigned scores. Nodes with higher scores are given priority for pod placement.

Binding: In the final phase, the scheduler selects the node with the highest priority and binds the pod to that node. The binding process ensures that the pod is scheduled to run on the chosen node.

These phases collectively help the scheduler make informed decisions about where to place pods in the cluster, considering factors like resource constraints, affinity rules, node health, and custom preferences defined by administrators or users. The goal is to optimize resource utilization and meet the requirements and constraints specified for each pod.


<h2>Prometheus and Grafana</h2>

Prometheus

Prometheus, a Cloud Native Computing Foundation project, is a systems and service monitoring system. It collects metrics from configured targets at given intervals, evaluates rule expressions, displays the results, and can trigger alerts when specified conditions are observed.

The features that distinguish Prometheus from other metrics and monitoring systems are:

- A multi-dimensional data model (time series defined by metric name and set of key/value dimensions)
- PromQL, a powerful and flexible query language to leverage this dimensionality
- No dependency on distributed storage; single server nodes are autonomous
- An HTTP pull model for time series collection
- Pushing time series is supported via an intermediary gateway for batch jobs
- Targets are discovered via service discovery or static configuration
- Multiple modes of graphing and dashboarding support
- Support for hierarchical and horizontal federation
- Architecture overview
- Architecture overview



![image](https://github.com/user-attachments/assets/3d7d98e2-52fe-453a-a412-10ef6fce7afc)


Grafana

Grafana allows you to query, visualize, alert on and understand your metrics no matter where they are stored. Create, explore, and share dashboards with your team and foster a data-driven culture:

- Visualizations: Fast and flexible client side graphs with a multitude of options. Panel plugins offer many different ways to visualize metrics and logs.
- Dynamic Dashboards: Create dynamic & reusable dashboards with template variables that appear as dropdowns at the top of the dashboard.
- Explore Metrics: Explore your data through ad-hoc queries and dynamic drilldown. Split view and compare different time ranges, queries and data sources side by side.
- Explore Logs: Experience the magic of switching from metrics to logs with preserved label filters. Quickly search through all your logs or streaming them live.
- Alerting: Visually define alert rules for your most important metrics. Grafana will continuously evaluate and send notifications to systems like Slack, PagerDuty, VictorOps, OpsGenie.
- Mixed Data Sources: Mix different data sources in the same graph! You can specify a data source on a per-query basis. This works for even custom datasources.


![image](https://github.com/user-attachments/assets/3326a187-1467-4a6b-bb49-ccfd6d2cb63d)



Somes Roles

![image](https://github.com/user-attachments/assets/7733a4f3-4608-4e55-9956-681c91d164a1)


Essentials Components

![image](https://github.com/user-attachments/assets/da96039b-c875-451e-a08e-ed3bc14722e4)

Importante: debemos profundizar en Prometheus and Graphana. 


Questions

Who was the original creator of Prometheus before it was donated to CNCF?
- Google
- SoundCloud (Correct)
- Microsoft
- IBM

The correct answer is: SoundCloud

Explanation:
Prometheus was originally created by SoundCloud in 2012 as an internal monitoring system. The team at SoundCloud needed a more robust and flexible monitoring tool, and thus, Prometheus was developed to handle their time-series data and monitoring requirements.

Prometheus gained popularity quickly due to its powerful query language (PromQL), its simplicity, and its design that catered well to modern, containerized environments. In 2016, Prometheus was donated to the Cloud Native Computing Foundation (CNCF), where it became one of the key projects in the cloud-native ecosystem.



What is the significance of the 'kube-prometheus operator’ project?
- It is a project for advanced Kubernetes networking
- It is a solution for setting up Kubernetes with Prometheus and Grafana (Correct)
- It is a Kubernetes security enhancement tool
- It is a Kubernetes cluster management interface

Explanation

The kube-prometheus-operator project is a set of Kubernetes manifests, tools, and operators designed to facilitate the deployment and management of Prometheus, Alertmanager, and Grafana on Kubernetes clusters. It provides a convenient way to set up monitoring and alerting for Kubernetes clusters using Prometheus as the metrics collection tool, Alertmanager for alerting, and Grafana for visualization.



What is the primary purpose of Kube-State-Metrics?
- To gather metrics about the state of objects via the Kubernetes API (Correct)
- To provide a user interface for Kubernetes cluster management
- To encrypt data communication between Kubernetes components
- To deploy and manage Prometheus within a Kubernetes cluster

Explanation

The correct answer is: To gather metrics about the state of objects via the Kubernetes API 

To gather metrics about the state of objects via the Kubernetes API. Kube-State-Metrics is a service that generates metrics about the state of various Kubernetes objects (like Pods, Deployments, Nodes, etc.) by querying the Kubernetes API. It doesn't collect metrics about the resource usage (like CPU or memory); instead, it focuses on the state of the Kubernetes resources.

  

What is the primary role of the Node-exporter in Prometheus?
- Managing database storage
- Providing hardware and OS metrics from the Kernel (Correct)
- Translating Kubernetes information to Prometheus metrics
- Generating visual graphs and charts

Explanation

The correct answer is: Providing hardware and OS metrics from the Kernel.

Node-exporter is a Prometheus exporter designed to gather and expose hardware and operating system (OS) metrics from the node (machine) where it is running. These metrics include details about the machine's resources such as CPU, memory, disk, network, and filesystem.

![image](https://github.com/user-attachments/assets/d71e4dbf-11d9-4155-b91e-175dfff12ffc)



What is the primary role of the Prometheus Adapter?
- To manage user access to Prometheus.
- To adapt Kubernetes information to Prometheus metrics (Correct)
- To serve as a database for Prometheus data
- To facilitate communication between Prometheus and external APIs


The correct answer is: To adapt Kubernetes information to Prometheus metrics.

Explanation: The Prometheus Adapter is primarily used in Kubernetes environments to enable custom metrics support for the Horizontal Pod Autoscaler (HPA) and other Kubernetes components that need to make decisions based on metrics stored in Prometheus.

Key Role of the Prometheus Adapter

- Custom Metrics: The Prometheus Adapter enables Kubernetes to use Prometheus metrics as custom metrics for scaling workloads, such as scaling pods based on custom application metrics that are collected by Prometheus.

- Adapter for HPA: It allows the Kubernetes Horizontal Pod Autoscaler to scale applications based on metrics that Prometheus is scraping. These custom metrics can include application-specific metrics (e.g., HTTP request count, custom business metrics) or even resource metrics that aren't part of Kubernetes' default metrics.

- API Interface: The adapter exposes Prometheus metrics through the Kubernetes metrics API. It translates queries to Prometheus into a format that Kubernetes understands, allowing it to scale resources based on the Prometheus data.



What is PromQL primarily used for in Prometheus?
- Managing user permissions
- Scheduling backup operations
- Querying and exploring metrics (Correct)
- Configuring alert notifications



The correct answer is: Querying and exploring metrics.

Explanation:
PromQL (Prometheus Query Language) is the powerful query language used in Prometheus to interact with the data it collects. PromQL allows users to query and explore time-series data stored by Prometheus, enabling them to:

- Retrieve Metrics: You can query specific metrics, apply filters, and aggregate data over time (e.g., average CPU usage over the last 5 minutes).
- Create Alerts: PromQL can be used to define alerting rules based on specific thresholds or conditions in the data.
- Explore Data: PromQL is used to visualize metrics directly in Prometheus' built-in web interface or in external tools like Grafana. It helps you explore metrics in real-time and perform ad-hoc analysis.
- Aggregation and Calculation: You can perform various mathematical operations on metrics, like summing up data across multiple instances, calculating rates, or computing percentiles.
- Common Use Cases of PromQL: Basic Queries: Extracting specific metrics (e.g., up{job="node"} to view the "up" status of node exporters).
- Aggregation: Summing or averaging metrics across multiple instances (e.g., avg(rate(http_requests_total[5m])) by (job) to get the average HTTP request rate for each job).
- Time Ranges: Working with time-series data over specific ranges (e.g., http_requests_total{status="500"}[1h] to get HTTP 500 errors in the last hour).
- Alerting: Defining conditions for triggering alerts based on metric values (e.g., avg(rate(cpu_usage[5m])) > 0.9 to alert if CPU usage is over 90%).


Grafana is primarily used for which of the following in an observability stack?
- Real-time performance analysis and troubleshooting
- Automated code deployment
- Data encryption and security
- Cloud infrastructure provisioning

Explanation: Ya tenemos las definiciones de Grafana y sus objetivos. 

Prometheus Components 

![image](https://github.com/user-attachments/assets/c30071d3-d45c-4f7a-9e80-453c02e91195)



<h2>Cost Management</h2>


Cost Management - Study Tips
For the KCNA exam, there are some key points which you will need to be aware about which are covered in this video -

Cloud Anomaly Detection
KubeCost as a tool for Cost Observability


![image](https://github.com/user-attachments/assets/2b9c7979-2e41-4527-8afe-50b7a424940e)



![image](https://github.com/user-attachments/assets/f6756a0d-3a01-4bcd-8f69-39a9c5ad61a8)


***Importante Leer y estudiar estos temas y sobre KubeCost tambien***

<h2>4 Key Challenges of Kubernetes Cost Management</h2>

    <ol>
        <li>
            <h2>1. Allocation of Total Costs</h2>
            <p>One of the primary challenges of Kubernetes cost management is the allocation of total costs to individual teams, projects, or applications. Kubernetes uses a shared resource model, which means that multiple teams or projects may be using the same cluster resources simultaneously. This makes it difficult to allocate costs accurately and fairly.</p>
            <p>To address this challenge, organizations need to implement a cost allocation model that accounts for shared resources and accurately reflects the usage of each team or project. This may include using tags, labels, or namespaces to track resource consumption and assigning costs proportionally.</p>
        </li>
        
        <li>
            <h2>2. Kubernetes Abstractions Reduce Transparency</h2>
            <p>Kubernetes abstracts away many of the underlying infrastructure details, which can make cost management more complex. For example, it is not always easy to map Kubernetes resources such as pods, nodes, and namespaces to specific cloud resources like virtual machines, storage, or networking. This can make it challenging to understand the costs associated with individual components and identify opportunities for optimization.</p>
            <p>To overcome this challenge, organizations should leverage Kubernetes management tools that provide deeper visibility into resource usage and cost data.</p>
        </li>
        
        <li>
            <h2>3. Multi-Cloud Environments</h2>
            <p>Many organizations are embracing multi-cloud strategies, deploying Kubernetes clusters across different cloud providers or on-premises infrastructure. While this approach provides increased flexibility and redundancy, it can also complicate cost management. Each cloud provider has its pricing model, and tracking costs across multiple environments can be a daunting task.</p>
            <p>To tackle this challenge, organizations need to adopt a unified approach to cost management that can provide insights across multiple cloud environments and ensure cost transparency and optimization.</p>
        </li>
        
        <li>
            <h2>4. Savings Insights and Opportunities</h2>
            <p>Identifying cost-saving opportunities in Kubernetes deployments requires a deep understanding of resource utilization patterns and potential inefficiencies. With dynamic scaling, auto-scaling, and the ephemeral nature of containers, it can be challenging to identify and act on these opportunities quickly.</p>
            <p>To address this challenge, organizations should invest in Kubernetes cost management tools that provide real-time visibility into Kubernetes costs, enabling them to make informed decisions on resource optimization.</p>
        </li>
    </ol>

<h1>Notable Kubernetes Cost Management Tools</h1>
    <p>Aquí hay algunas herramientas de gestión de costos de Kubernetes que vale la pena revisar.</p>

    <h2>Komodor</h2>
    <p>Komodor’s cost optimization suite ensures visibility, optimization and responsible Kubernetes growth without compromising on performance, all from the same Kubernetes platform you know and love.</p>
    <ul>
        <li><strong>Gain Visibility & Allocate Costs Across Your K8s Environment:</strong> Keep a close eye on your Kubernetes cost breakdown and monitor resource consumption with ease. By allocating costs based on business units, teams, environments, and applications, you gain a clearer understanding of spending patterns. Analyzing cost trends over time empowers you with valuable insights, enabling you to identify areas for optimization and potential savings. Our user-friendly approach ensures that you can readily comprehend your cost efficiency, making it easier to promote accountability and transparency within your organization.</li>
        <li><strong>Optimize Costs Rightsize the Perfect Balance Between Costs & Consumption:</strong> Our solution offers a range of powerful features to optimize your resource usage efficiently. By analyzing real-time usage in comparison to requirements, you can ensure optimal resource allocation. Identify and address any missing requests and limits to streamline performance and avoid wastage. Eliminate idle resources that are not contributing to your operations, boosting efficiency. Tailoring optimization strategies to each environment ensures maximum impact. With just one click, you can apply our intelligent recommendations and experience significant time and cost savings, simplifying the process and reducing potential challenges.</li>
        <li><strong>Ensure Reliability Monitor the Impact of Your Optimization:</strong> Our proactive monitoring system allows you to maintain continuous operations with optimized resources. By actively monitoring your resources, we can promptly identify and flag availability concerns, out-of-memory issues, or CPU throttling, ensuring the smooth functioning of your systems. Receive timely alerts directly to your ticketing and instant messaging applications, keeping you informed of any potential issues. Our integrated approach helps you avoid silos and effortlessly connect performance and cost data in one centralized location, streamlining your management and decision-making processes for improved efficiency.</li>
    </ul>
    <p>Learn more about Komodor for Kubernetes cost optimization or get started now!</p>

    <h2>Kubernetes Dashboard</h2>
    <p>The Kubernetes Dashboard is an open-source web-based user interface for Kubernetes clusters. It provides a comprehensive view of your cluster’s resources and allows you to manage them effectively. Some of the key features of the Kubernetes Dashboard for cost management include:</p>
    <ul>
        <li><strong>Resource monitoring:</strong> The Kubernetes Dashboard allows you to monitor your cluster’s resource usage in real-time. You can view CPU, memory, and storage utilization, as well as the number of running containers and pods. This data can help you identify potential bottlenecks and optimize your resource usage.</li>
        <li><strong>Resource scaling:</strong> With the Kubernetes Dashboard, you can easily scale your deployments up or down based on your resource needs. This ensures that you only pay for the resources you actually need and helps you reduce your overall spending.</li>
        <li><strong>Cost analysis:</strong> By using the Kubernetes Dashboard in conjunction with other cost management tools, such as Prometheus and Grafana, you can gain insights into your cluster costs. This can help you identify areas where you can reduce spending and optimize resource usage.</li>
    </ul>
    <p><em>Source: Kubernetes</em></p>

    <h2>Kubecost</h2>
    <p>Kubecost is another popular Kubernetes cost management tool that provides real-time cost insights and optimization recommendations. It offers several features to help you manage your Kubernetes costs, including:</p>
    <ul>
        <li><strong>Cost allocation:</strong> Kubecost enables you to allocate costs based on various parameters, such as namespaces, labels, or annotations. This helps you understand which applications or teams are consuming the most resources and make informed decisions on resource allocation.</li>
        <li><strong>Cost monitoring:</strong> Kubecost offers a dashboard that displays your cluster costs in real-time. You can view your spending by various dimensions, such as cloud provider, region, or instance type.</li>
        <li><strong>Cost forecasting:</strong> Kubecost provides cost forecasting capabilities that help you predict your future spending based on your historical data. This enables you to plan your budgets more effectively and avoid unexpected cost overruns.</li>
        <li><strong>Resource optimization:</strong> Kubecost offers optimization recommendations to help you reduce your cluster costs. These suggestions can include resizing your nodes, adjusting your auto-scaling settings, or eliminating unused resources.</li>
    </ul>
    <p><em>Source: Kubecost</em></p>

    <h2>Cast.ai</h2>
    <p>Cast.ai is a Kubernetes cost management and optimization platform that utilizes machine learning algorithms to help you reduce your cloud spending. It offers several features to help you manage your Kubernetes costs, including:</p>
    <ul>
        <li><strong>Cost allocation:</strong> Cast.ai allows you to allocate costs based on various parameters, such as namespaces, labels, or annotations. This helps you understand which applications or teams are consuming the most resources and make informed decisions on resource allocation.</li>
        <li><strong>Cost monitoring:</strong> Cast.ai offers a dashboard that displays your cluster costs in real-time. You can view your spending by various dimensions, such as cloud provider, region, or instance type.</li>
        <li><strong>Cost forecasting:</strong> Cast.ai provides cost forecasting capabilities that help you predict your future spending based on your historical data. This enables you to plan your budgets more effectively and avoid unexpected cost overruns.</li>
        <li><strong>Resource optimization:</strong> Cast.ai uses machine learning algorithms to optimize your Kubernetes clusters automatically. This can include resizing your nodes, adjusting your auto-scaling settings, or eliminating unused resources. By automating the optimization process, Cast.ai helps you save time and reduce your operational costs.</li>
    </ul>
    <p><em>Source: Cast.ai</em></p>

    <h2>Conclusion</h2>
    <p>In conclusion, Kubernetes cost management is a critical facet of utilizing Kubernetes, a popular platform for managing containerized applications. As businesses strive to get the most out of their investment, they face challenges such as allocating costs fairly among teams, dealing with Kubernetes’ infrastructure abstractions, managing costs in multi-cloud environments, and promptly identifying savings opportunities.</p>
    <p>Thankfully, there’s a plethora of tools available to help organizations navigate these challenges. These Kubernetes cost management tools not only provide transparency and control over costs but also help pinpoint inefficiencies, make data-driven decisions, and optimize resource allocation.</p>
    <p>By leveraging these tools, businesses can align their technical operations with their financial goals, maximize the ROI from their Kubernetes deployments, and ensure optimal resource utilization. However, the choice of tool should be made carefully, taking into account the specific needs, resources, and complexity of the organization’s Kubernetes deployments. With the right strategies and tools, Kubernetes cost management can become a strategic advantage, driving both operational efficiency and financial health.</p>




 <h2>Questions</h2>

 What is a primary benefit of designing applications in a Cloud Native manner?
 - They can only run on private clouds
 - They are restricted to a single public cloud provider
 - They can run across different public, hybrid, and private cloud offerings (Correct)
 - They are automatically compliant with all regulatory requirements


Which of the following is a characteristic of On-Demand instances in cloud computing?
- They are the least expensive option
- They require long-term commitment
- They can be spun up in seconds and disposed of as needed  (Correct)
- They are primarily used for long-term, stable workloads

Explanation

The correct characteristic of On-Demand instances in cloud computing is: They can be spun up in seconds and disposed of as needed.
On-Demand instances are designed to be flexible and cost-effective for short-term, variable workloads. You only pay for the compute capacity you use, and there is no long-term commitment or upfront cost. These instances are ideal for workloads that have unpredictable traffic or that need to be quickly scaled up or down.



What is a key consideration when using Reserved Instances in cloud computing?
- They offer no cost savings over On-Demand instances
- They require bidding for instance availability
- They involve upfront payment for a committed period with potential cost savings (Correct)
- They are suitable for unpredictable, short-term workloads

Explanation

The correct key consideration when using Reserved Instances in cloud computing is: They involve upfront payment for a committed period with potential cost savings.
Reserved Instances (RIs) allow you to commit to using a certain instance type in a specific region for a set period, usually one or three years. In exchange for this commitment, you can receive significant cost savings compared to On-Demand instances.



What is a significant risk associated with using Spot Instances in cloud computing?
- They are the most expensive option
- There is no guarantee of instance availability  (Correct)
- They require a long-term commitment
- They do not allow for autoscaling

Explanation

The correct answer is: There is no guarantee of instance availability.
Spot Instances are a cost-effective option in cloud computing because they allow you to bid for unused capacity. However, the significant risk is that there is no guarantee these instances will remain available.


What is the concept of 'Right Sizing' in the context of cloud computing?
- Migrating to the cloud with the same infrastructure as on-premises
- Always choosing the cheapest cloud resources available
- Scaling cloud resources based on actual usage and needs (Correct)
- Using only Reserved Instances for all cloud workloads

Explanation

The correct concept of 'Right Sizing' in the context of cloud computing is: Scaling cloud resources based on actual usage and needs.

Right Sizing involves selecting the appropriate instance types, sizes, and configurations based on the actual performance and usage requirements of your workloads. It ensures you're not over-provisioning (which wastes resources) or under-provisioning (which can lead to performance issues), optimizing both cost and efficiency. This approach helps ensure that your cloud infrastructure matches the specific demands of your applications, avoiding unnecessary expenses.



Which aspect of cloud cost management is enhanced by detecting cloud anomalies?
- Ensuring uninterrupted service availability
- Improving the physical security of cloud data centers
- Keeping costs under control by identifying unexpected charges  (Correct)
- Simplifying the user interface of cloud management tools

The correct answer is: Keeping costs under control by identifying unexpected charges.
Detecting cloud anomalies helps in identifying unusual or unexpected usage patterns that could result in higher-than-expected charges. This can include things like unexpected resource usage, misconfigured services, or sudden spikes in traffic.


What is a primary function of KubeCost in cloud-native environments?
- It serves as the main database for Kubernetes
- It automatically scales cloud resources up and down
- It helps in monitoring and managing Kubernetes costs  (Correct)
- It enhances the security of Kubernetes clusters



ContainerD/CRI-O
ContainerD:

- ContainerD is an industry standard container runtime with emphasis on simplicity, robustness and portability

- This includes Docker's functionality for executing containers, low-level storage & managing image transfers.

- ContainerD makes it easier for projects like K8s to access the low-level "Docker" elements they need

- Images built with Docker aren't really "Docker image"

- Images are built in the standardized OCI format.

![image](https://github.com/user-attachments/assets/9ba29aa1-b2ca-4d97-91ad-fb38129b0b64)



ContainerD logo
CRI-O
Alternative to using Docker

It supports runc & kata containers as container runtimes



<h1>Las diferencias entre Docker, containerd, CRI-O y runc</h1>

    <p>Los contenedores no están estrechamente vinculados al nombre Docker. Puedes usar otras herramientas para ejecutar contenedores.</p>

    <p>Puedes estar ejecutando contenedores con Docker, o un montón de otras herramientas que no son Docker. Docker es solo una de las muchas opciones, y Docker (la compañía) crea algunas de las herramientas más geniales del ecosistema, pero no todas.</p>

    <h2>Existen dos grandes estándares alrededor de los contenedores:</h2>

    <ul>
        <li><strong>Open Container Initiative (OCI)</strong>: un conjunto de estándares para contenedores, que describe el formato de las imágenes, el runtime y la distribución.</li>
        <li><strong>Container Runtime Interface (CRI) en Kubernetes</strong>: una API que permite usar diferentes runtimes de contenedores en Kubernetes.</li>
    </ul>

![image](https://github.com/user-attachments/assets/254d5c33-ab2c-43fd-af39-f479819dd154)


<h3>How the Docker stack works</h3>

Docker Engine comes with a bunch of tools to make it easy to build and run containers as a developer, or a systems administrator. It is basically a command-line interface (CLI) for working with containers.

So, in reality, when you run a container with docker, you’re actually running it through the Docker daemon, which calls containerd, which then uses runc.

But the docker command is just one piece of the puzzle. It actually calls down to some lower-level tools to do the heavy lifting:


![image](https://github.com/user-attachments/assets/fd1d2ae0-2fa7-4ccf-9d33-d1289f323b57)



What are the lower-level tools in the Docker stack?
From the bottom up, these are the tools that docker uses to run containers:

Lowest-level 🔩 The low-level container runtime. runc is a low-level container runtime. It uses the native features of Linux to create and run containers. It follows the OCI standard, and it includes libcontainer, a Go library for creating containers.
🔧 The high-level container runtime. containerd sits above the low-level runtime, and adds a bunch of features, like transferring images, storage, and networking. It also fully supports the OCI spec.
👺 The Docker daemon. dockerd is a daemon process (a long-running process that stays running in the background) which provides a standard API, and talks to the container runtime
Highest level 👩‍💻 The Docker CLI tool. Finally, docker-cli gives you the power to interact with the Docker daemon using docker ... commands. This lets you control containers without needing to understand the lower levels.
Does Kubernetes use Docker?
A really common question is “how do containers run in Kubernetes?”. Does Kubernetes use Docker? Well, it doesn’t anymore — but it used to.

Originally, Kubernetes used Docker (Docker Engine) to run containers.

But, over time, Kubernetes evolved into a container-agnostic platform. The Container Runtime Interface (CRI) API was created in Kubernetes, which allows different container runtimes to be plugged into it.

Docker Engine, being a project older than Kubernetes, doesn’t implement CRI. So to help with the transition, the Kubernetes project included a component called dockershim, which allowed Kubernetes to run containers with the Docker runtime.

It bridged the gap between the old world and the new.

Death of the shim also
But, as of Kubernetes 1.24, the dockershim component was removed completely, and Kubernetes no longer supports Docker as a container runtime. Instead, you need to choose a container runtime that implements CRI.

The logical successor to Docker Engine in Kubernetes clusters is… containerd. (10 points if you got that correct!) Or you can use an alternative runtime, like CRI-O.

This doesn’t mean that Kubernetes can’t run so-called Docker-formatted containers. Both containerd and CRI-O can run Docker-formatted and OCI-formatted images in Kubernetes; they can do it without having to use the docker command or the Docker daemon.

Open Container Initiative (OCI) specifications
The OCI was one of the first efforts at creating some standards for the container world. It was established in 2015 by Docker and others.

The OCI is backed by a bunch of tech companies and maintains a specification for the container image format, and how containers should be run.

For example: you might use one OCI-compliant runtime for your Linux hosts, but a different runtime for your Windows hosts.

Kubernetes Container Runtime Interface
The other standard we need to talk about is the Container Runtime Interface (CRI). This is an API that was created by the Kubernetes project.

CRI is an interface used by Kubernetes to control the different runtimes that create and manage containers.


![image](https://github.com/user-attachments/assets/150da967-47cc-4abb-81f5-e98f9ed3c1d2)



So if you prefer to use containerd to run your containers in Kubernetes, you can! Or, if you prefer to use CRI-O, then you can. This is because both of these runtimes implement the CRI specification.

But, if you pay to get support (security, bug fixes etc) from a vendor, your choice of container runtime might be made for you. For example, Red Hat’s OpenShift uses CRI-O, and offers support for it. Docker provides support for their own containerd.

containerd and CRI-O
We’ve seen that Docker Engine calls down to a bunch of lower-level tools. But what are these tools? And how do they fit together?

The first layer is the high-level runtimes: containerd, created by Docker, and CRI-O, created by Red Hat.

containerd
containerd is a high-level container runtime that came from Docker. It implements the CRI spec. It pulls images from registries, manages them and then hands over to a lower-level runtime, which uses the features of the Linux kernel to create processes we call ‘containers’.

CRI-O
CRI-O is another high-level container runtime which implements the Kubernetes Container Runtime Interface (CRI). It’s an alternative to containerd. It pulls container images from registries, manages them on disk, and launches a lower-level runtime to run container processes.

Yes, CRI-O is another container runtime. It was born out of Red Hat, IBM, Intel, SUSE .

runc and other low-level runtimes
runc is an OCI-compatible container runtime. It implements the OCI specification and runs the container processes.

runc is sometimes called the “reference implementation” of OCI.

Other low-level runtimes
But, runc isn’t the only low-level runtime. The OCI specification is allowing other tools to implement the same functionality in a different way:

crun a container runtime written in C (by contrast, runc is written in Go.)
firecracker-containerd from AWS, which implements the OCI specification as individual lightweight VMs (and it is also the same technology which powers AWS Lambda)
gVisor from Google, which creates containers that have their own kernel. It implements OCI in its runtime called runsc.

Otras imagenes para saber la diferencia entre CRI-O, Containerd etc

![image](https://github.com/user-attachments/assets/c817ff6c-41a2-4edc-8ad9-9b727a4e736c)

![image](https://github.com/user-attachments/assets/c2143846-206c-4a0a-b0c4-9ac310c356db)


![image](https://github.com/user-attachments/assets/415883a8-5450-447c-8d27-ee54442c05f5)

![image](https://github.com/user-attachments/assets/6db6d12d-03a7-464e-8743-de3dc632008f)

![image](https://github.com/user-attachments/assets/126a8b3e-97c7-470e-a746-08be824a45f9)


<h2>Cloud Native Application Delivery and GitOps</h2>

Cloud Native Application Delivery and GitOps - Study Guide
As part of your KCNA study, these are the main points of consideration for the Cloud Native Application Delivery and GitOps section -

Be aware of Argo and how this software integrates with the GitOps lifecycle
Knowledge that Argo can be further utilised through the use of Argo Workflows
Have an understanding and awareness of Flux, an Argo alternative
Have an understanding of the GitOps toolkit which Flux utilises




