## Welcome to Docker

Mixa i Sale

---

### What is Docker?

Docker is an **open-source** project that automates the deployment of applications inside **software containers**. (Wikipedia)

---

### What are software contaners?

Containers are a method of **operating system** **virtualization** that allow you to run an application and its **dependencies** in **resource-isolated** processes. (AWS)

---

### What is an operating system?

Operating systems provide a software platform on top of which other programs, called application programs, can *run*.

What does a program need in order to run?
- CPU
- Memory
- Storage
- Network
- ...

---

### What is virtualization?

In computing, virtualization refers to the act of creating a virtual (rather than actual) version of something, including virtual computer hardware platforms, storage devices, and computer network resources. (Wikipedia)

It is all about resource control.

---

### What are application/program/process dependencies?

- Libraries
- Runtime (java, ruby, node, dotnet...)
- Other applications (cron, ffmpeg, mysqld, mongod...)

---

### What is resource-isolated?

Isolated - separated from other persons or things; alone; solitary.

This is about limiting what process can see:
- What part of the root file system?
- What network?
- What devices?
- ...

---

### So, what are software contaners?

A way to tell operating system to start a process with access to only specific fake resources totally separated from the rest of the system and to limit its usage of real system resources (number of CPU cores, amount of memory, storage size, storage and network read/write speed).

---

### How is this possible?

Linux kernel has two features that make this possible: **cgroups** and **namespaces**.

Cgroups provide resource **limiting** and monitoring, including the CPU, memory, block I/O, and network.

Namespaces **isolates** an application's view of the operating environment, including process trees, network, user IDs and mounted file systems.

---

### Containers != VMs

VMs are about running full OS on top of another OS.

Containers are about running a **single process**.

![](files/docker-containers-vms.png)

---

### Containers != VMs

- **There are no performance losses when running a process inside a container**
- Containers can be started in seconds
- Contaner size is measured in MBs
- You can run many (hundreds) containers on a single machine

---

### How to make containers usefull?

The goal of containers is to to create a universal mechanism of deploying an app **anyware**.

In order to do this we need a way of describing what certain app needs (its dependencies) and to package all that together. This is defined in a **Docker Image**.

Docker image is a tar archive that contains a json manifest file and the whole file system needed for an app to run and also describes how to actually start the app.

---

### How to create an image?

An image is created (built) by executing a set of instructions defined in a **Dockerfile**. This is done by **Docker CLI**.

Dockerfile
```
FROM scratch
COPY hello /
CMD ["/hello"]
```

Docker build image
```
$ docker build -f /path/to/a/Dockerfile .
```

---

### How to start a process from an image?

In order to start a process we need some program (a runtime) that can interpret the content of an image and use cgroups and namespaces to **create a container** for it and then run the process inside. This is done by a **Docker Engine**.

One of the key features of Docker Engine is its REST api which enables secure remote control and monitoring.

---

### How to deliver an image to an engine?

An image can be build by the cli and delivered to an engine directly through the API, but it is much more usefull to have one central place where somebody can submit an image and than any engine can pull that image and build a container from it. This central place for storing images is **Docker Repository**.

There are many docker repositories: Docker Hub, Quay, AWS ECR, GCP CR or build your own.

---

### How to deliver an image to an engine?

Push an image to a repo
```
$ docker images

REPOSITORY            TAG                 IMAGE ID            CREATED             SIZE
test_img              latest              a9bea64bd24f        10 days ago         50 MB

$ docker tag a9bea64bd24f {aws_account_id}.dkr.ecr.{region}.amazonaws.com/{my-web-app}

$ docker push {aws_account_id}.dkr.ecr.{region}.amazonaws.com/{my-web-app}
```
---

Pull an image
```
$ docker pull {aws_account_id}.dkr.ecr.{region}.amazonaws.com/{my-web-app}
```

Create a contaner to run the app
```
docker run --name {my-web-app-0} -d {aws_account_id}.dkr.ecr.{region}.amazonaws.com/{my-web-app}
```

---

### Why is this important?

- This is a universal deployment method for any app - it works with any language/framework.
- Docker containers are supported by all IaaS and PaaS providers (AWS, MS, GCP...)
- Replicate production env on development machine (Docker Compose). And you can do this for many different projects.
- Build highly available and scalable systems with container clastering solutions (Docker Swarm, Kubernetes, AWS ECS)
- Security - everything is isolated so you can run it without worrying about the rest of the system. Containers make it possible to build:
  - CI systems
  - PaaS (Heroku)
  - Cloud functions/lamdas
  - ...

---

# DEMO

---

# Q&A

---

# HVALA :)