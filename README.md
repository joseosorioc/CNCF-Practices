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
