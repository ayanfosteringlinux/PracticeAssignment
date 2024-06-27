![1_JAJ910fg52ODIRZjHXASBQ](https://github.com/ayanfosteringlinux/StuFFs/assets/153751979/0156be78-d677-4187-9d9d-f8396ffda1a8)


# Docker
 Prior moving towards what is ```Docker```? , lets start from ```HyperVisor``` as ```Docker``` itself is based on virtualization.

 <br>

 >**HyperVisor**

 It is a piece of software / firmware that creates and run Virtual-Machine. A ```HyperVisor``` is sometimes also called a ```Virtual Machine Manager```(VMM). Hypervisors can support both 32-bit and 64-bit systems, though many modern hypervisors are designed for 64-bit systems due to their enhanced capabilities and performance.

 <br>

 # Types of HyperVisor

 Basically, there are two types of ```HyperVisor``` .

 * Type - 1 HyperVisor
 * Type - 2 HyperVisor

 <br>

>**Type - 1 HyperVisor**

* It is also called ```Bare Metal HyperVisor```.
* It runs directly on the system/host hardware.
* Guest O.S run on another level above ```HyperVisor```.
* It acts as their own O.S

  <u>Example</u> : VMware ESXi etc.

  <br>

>**Type - 2 HyperVisor**

* It runs within a conventional O.S environment which the host O.S provides.
* It doesn't have direct access to host hardware & resources.
  
  **Example:** VMware Workstation, Oracle VB, Microsoft Virtual PC etc.

  <br>

>Now let's move ahead to know what actually ```Docker``` is.

<br>

# **Docker-Engine**


>Docker is a platform used for developing, shipping, and running applications. It uses containerization technology to package software into standardized units called containers.It is an advanced version of Virtualization. Containers are lightweight, portable, and isolated environments that contain everything needed to run an application, including the code, runtime, system tools, libraries, and settings.

<br>

# **Key features of Docker include:**


>**Containerization:** 

Docker containers encapsulate applications and their dependencies, allowing them to run in isolated environments without affecting other applications or the host system.

>**Portability:** 

Docker containers can run on any system with the Docker engine installed, providing consistent behavior across different environments.

>**Efficiency:** 

Docker containers are lightweight and share the host system's kernel, enabling efficient resource utilization and faster startup times compared to virtual machines.

>**Scalability:** 

Docker makes it easy to scale applications by quickly deploying additional containers to handle increased demand.

>**Developer productivity:** 

Docker simplifies the development process by providing a consistent environment for building, testing, and deploying applications.

<br>

# Docker Architecture & Container

* Docker is developed by ```Solomen Hykes``` & ```Sebastian Pahl``` in the month of ```March in 2013```.
 
* Docker was developed by Solomon Hykes and the team at Docker, Inc. (initially called dotCloud).

* Docker is an open-source centralized platform designed to create, deploy & run applications.

* Docker is a set of platfrom as a service that uses O.S - level Virtualization. Whereas VMware uses hardware - level Virtualization.

* Docker uses Container on the host - O.S to run applications. It allows applications to use the same Linux kernel as a system on the host computer, rather than creating a whole virtual O.S . 

* You can install Docker on any O.S but ```Docker-Engine``` runs natively on ```Linux``` distro's.

* Docker is written in ```GO``` language.

* Docker is a tool that performs O.S level virtualization also known as ```Containerization```.

* Before ```Docker```, many users were facing issues that a particular code is running in the developer's system but not in the user's system.

<br>

 # Advantages of Docker

>No Pre-Allocation of RAM needed.

>CI Efficiency - Docker enables users to build a container image and use it across every step of the deployment process.

>Cost - Efficient

>Light - Weight (occupies less resource)

>It can run on physical / virtual / H/W or on cloud.

>User can re-use the ```image```.

>It takes less time to create container.

<br>

# Disadvantages of Docker

* It is not a good solution fo app that requires rich ```GUI```

* Difficult to manage large amount of container.

* It does not provide cross-platform compatibility, means if an app is designed to run on ```Windows```, then it can not run on ```Linux``` or (vice-versa).

* It is suitable when both ```developer O.S``` & ```testing O.S``` are same. If ```O.S``` is different then use ```VM```.

* No solution for ```Data Recovery``` & ```Backup```.

<br>

 # Architecture

 <br>

 **Components of Docker**

 <hr>

**1.Docker Daemon**

* Docker Daemon runs on the ```Host O.S```.

* It is responsible for running containers to manage docker services.

* It can communicate with other ```daemons```.

<br>

**2.Docker Client**

* Docker users can interact with ```Docker Daemon``` through a client ```(CLI)```.

* Docker client uses commands(CLI) & rest  ```API``` to communicate with docker daemon.

* When a client runs any command on the docker client terminal, the client terminal sends these docker commands to the docker daemon.

* It is possible for docker client to communicate with more than one daemon.

<br>

**3.Docker Host**

* Docker host is used to provide an environment to execute and run applications.

* It contains the docker daemon, images, containers, networks and storages.

<br>

**4.Docker Hub/Registry**

Docker registry manages and stores(private) the docker images.

There are two-types of registries in the docker.

* Public Registry - It is also called as ```Docker Hub```.

* Private Registry - It is used to share images within the enterprise.

<br>

**5.Docker Images**

They are the read only binary templates used to create docker containers.

**<u>OR</u>**

Single file with all ```dependencies``` and configuration required to run a program/container.

**<u>Ways to create an IMAGE</u>**

* Take image from docker hub.

* Create image from docker file.

* Create image from existing docker containers.

<br>

**6.Docker Container**

* Container holds the entire packages that is needed to run the application.

<u>OR</u>

* In other words, you can say that the image is a template and the container is a copy of that template.


* Container is like a Virtual Machine.

* Images becomes container when they run on docker engine.

<br>

# Basic Commands in Docker

**To list ```images``` present in your local machine.**
```bash
$ docker images
```
<hr>
<br>

**To find out ```images``` in ```docker-hub```.**
```bash
$ docker search <image-name>
```

**For ex:-**
``` $ docker search ubuntu```

<hr>
<br>

**To pull image from ```docker-hub``` to your local machine.**

```bash
$ docker pull <image-name>
```
<hr>
<br>

**To give a desired name to container prior running it.**

```bash
$ docker run -it --<desired-name> <image-name> /bin/bash
```
**For ex:-** ```docker run -it --my_container ubuntu /bin/bash```

<hr>
<br>

**To check service status of** ```docker-engine```.

```bash
$ service docker status
```
<hr>
<br>

**To start container**

```bash
$ docker start <comtainer-name>
```
**For ex:-** ```docker start my_container```

<hr>
<br>

**To stop container**

```bash
$ docker stop <container-name>
```
**For ex:-** ```docker stop my-container```

<hr>
<br>

**To delete container**

```bash
$ docker rm <container-name>
```
**For ex:-** ```docker rm my-container```

<hr>
<br>

**To go inside container**

```bash
$ docker attach <container-name>
```
**For ex:-** ```docker attach my_container```

<hr>
<br>

**To list all containers**

```bash
$ docker ps -a
```
<hr>
<br>

**To list only running containers**

```bash
$ docker ps
```

<br>

# Docker ```diff``` command

To inspect the difference between the base image & the changes made on it, you can use the ```diff``` command to inspect.

```step-1:``` Login to docker viaa CLI.

```step-2:``` Create container from an image.
 
  ```bash
  $ docker run -it --name <container-name> <image-name> /bin/bash
  ``` 

```step-4:```
  ```bash
  $ cd tmp/
  ```

```step-5:``` Create a file inside the ```tmp``` directory.
```bash
touch my-file
```

```step-6:``` Now, If you want to check or inspect the difference b/w the base image & changes on it, then you can use the below commands.

```bash
$ docker diff <container-name> <image-name>
```
```Output:```

```
C /usr/bin/python3.9
A /app/main.py
D /var/lib/dpkg/status
```
<br>

>**Explanation of the Lines:**

<hr>
<br>

* **C /usr/bin/python3.9:** This line indicates that the file /usr/bin/python3.9 has been changed ```(C)``` within the container compared to its original image.

* **A /app/main.py:** This line shows that the file /app/main.py has been added ```(A)``` to the container and isn't present in the base image.

* **D /var/lib/dpkg/status:** This line signifies that the file /var/lib/dpkg/status has been deleted ```(D)``` from the container.


<br>

<u>**Remarks :**</u>

>**A - append/add**<br>
**C - change**<br>
**D - deletion**<br>
**M - modify**<br>

```step-7:``` Now create an image of this container.

```bash
docker commit <container-name> <image-name>
```

```step-8:``` Now create a container from the image you built in ```step-7```.

```bash
$ docker run -it --name <container-name> <image-name> /bin/bash
```
```Output:```

``` 
root@user:~$ ls
root@user:~$ cd tmp/
root@user:~/tmp$ ls
root@user:~/tmp$  my-file
```
Now, you will see the file ```my-file``` in this container also, which you had created in previous container.

<br>

# Dockerfile & Its Components

<br>

**1. Dockerfile :**

>A Dockerfile is a text document that contains instructions for building a Docker image. It serves as a blueprint that defines the steps to be followed for creating a standardized, reproducible unit of software. Here's a breakdown of Dockerfiles and their key characteristics:

<br>

**2. Dockerfile Components :**

```FROM``` : It is used for base image. This instruction must be on top inside the dockerfile.

```RUN``` : It contains commands to be executed while creating image. It will create layers in image.

```MAINTAINER``` : Author / Owner / Description

```COPY``` : Copy files from host system. User needs to provide source path & destination path.

```ADD``` : It is similar to ```COPY``` but it provides a feature to download files from ```docker-hub```.

```EXPOSE``` : It is used to export ports such as ```8080``` for tomcat, ```80```for nginx etc.

```WORKDIR``` : It is used to set a working directory for container.

```CMD``` : It also contains executable commands similar to ```RUN``` but it contains commands to be executed after container creation.

```ENTRYPOINT``` : Similar to ```CMD``` but has higher priority over ```CMD```. In the list of executable command, first command will be executed by ```ENTRYPOINT``` only.

```ENV``` : Contains environment variables. Defines run-time variable.

```ARG``` : Defines variables. It is used to define build-time variable.


# Dockerfile Format

```Step-1:``` Create a file named "Dockerfile".

```Step-2:``` Add instructions in "Dockerfile".

```Step-3:``` Build "Dockerfile" to create image.

```Step-4:``` Run image to create container.

<br>

>**Steps-Explained :**

```Step-1:``` Create a file named "Dockerfile".
```bash
sudo vim Dockerfile
```

```Step-2:``` Add instructions in "Dockerfile".

```
FROM ubuntu:20.0
RUN echo Lorem Ipsum >/tmp/testfile
```

```Step-3:``` Build "Dockerfile" to create image.

```
docker build -t myimage .
```

```Step-4:``` Run image to create container.

```
 docker run -it --name mycontainer myimage /bin/bash
 ```

 ```bash
 cd /tmp
 ls
 testfile
 cat testfile
 ```

 You can see that the instructions you had written in ```RUN``` to creata a directory named testfile and fill it with ```Lorem Ipsum``` is now available in that container.

<br>

 # Docker Volume

 * Volume is simply a directory inside a container.

 * First, we have to declare the specified directory as a volume and the share volume.

 * Even if we stop a container, still we can access volume.

 * Volume will be created in on container.

 * You can declare a directory as a volume only while creating container.

 * You can't create volume from existing container.

 * You can share one volume across any number of containers.

 * Volume will not be included when you update an image.

 * You can map volume into container in two ways.
     1. Container ⇌ Container
     2. Host ⇌ Container

<br>

# Benifits of Docker Volume   

* Decoupling container from storage

* Share volume among different containers

* Attach volume to container

* On deleting container, volume will not be deleted

<br>

# Creating Volume via Dockerfile

```Step-1:```  Create a file named "Dockerfile".

<br>

```Step-2:``` Add instructions in "Dockerfile".

Example-

```
FROM ubuntu:20.0
VOLUME /myvolume
```
<br>

```Step-3:``` Build "Dockerfile" to create image.

```
docker build -t myimage .
```
<br>

```Step-4:``` Run image to create container.

```
docker run -it --name mycontainer myimage /bin/bash
```
<br>

```Step-5:``` Verify volume.

Verify the volume is reflected in container by using command ```docker volume ls```.

<br>

```Step-6:``` Share volume across containers.

```
docker run -it --name newcontainer --privileged=true --volumes-from mycontainer myimage /bin/bash
```
<br>

```Step-7:``` Now after creating new container ```newcontainer```, we can access volume from ```mycontainer``` and the data saved in ```myvolume``` will be dynamic from both sides either ```mycontainer``` or ```newcontainer```.

<br>

# Creating Volume via CLI

```Step-1:```  Enter the following commands in your terminal and hit enter key.

```bash
docker run -it --name mycontainer -v /myvolume myimage /bin/bash
```
<br>

```Step-2:``` Do ```ls``` and enter the directory named ```myvolume``` to verify that it is created.

```Step-3:``` Now create a container & share the volume```myvolume```.

```bash
docker run -it --name newcontainer --privileged=true --volumes-from mycontainer myimage /bin/bash
```

```Step-4:``` After entering   ```newcontainer```, we can access volume from ```mycontainer``` and the data saved in ```myvolume``` will be dynamic from both sides either ```mycontainer``` or ```newcontainer```.

# Volume (Host ⇌ Container)

```Step-1:```  Verify files in ```/home/user```.

```Step-2:```  Run the below command

```bash
docker run -it --name hostcontainer -v /home/user:/tmp --privileged=true myimage /bin/bash
```

```Step-3:```  Verify files in ```/tmp```.

```bash
cd /tmp
```

```Step-4:```  Do ```ls```, now you can see the files of host.

# Docker Port Exposing

```Step-1:```  Create a container while exposing it to desired port.

```bash
docker run -it --name mycontainer -p 8080:80 myimage
```
Where ```8080``` port of host machine is exposed to ```80``` port of container.

```Step-2:```  Verify the port exposed.

```bash
docker ps
```
It will list the running containers with port exposed.

```Step-3:```  Verify the exposed port individually.

```bash
docker port mycontainer
```
Output:

```
80/TCP -> 0.0.0.0:8080
```
<br>

# Congrats

Now, you have enough knowledge of what Docker is and how it works.

<br>

**Thanks & Regards <br>
Belal Ahmad Kureshi <br>
KeenAble Computers Pvt. Ltd.**
