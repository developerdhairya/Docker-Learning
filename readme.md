# **Docker Learning**

### *Docker is nothing but a platform for running,building and shipping containers.*

- Before diving into docker it is very important to be crystal clear about the difference between two things that is *`virtual machine`* and *`container`*.

- **Virtual Machine**:Virtual machine is just an abstration of physical hardware. We can run several isolated virtual machnes on a single physical machine. Suppose if you have a macbook machine you can run both Windows & Linux on top of it using a tool called hypervisor which is a software to create and  manage virtual machines. Some of commonly used hypervisors are Virtual Box and VMware.

- **Container**:A container is a nothing just an operating system virtualization.It is standalone unit of software that packages up code and all dependencies an application will require to run.It provides us an isolated environment for running applications on a single operating system.

- A docker container technically an OS process having its own file system and all containers share kernel of host OS.

- Before the advent of docker,there often arised situations where an application runs on a developer's machine but fails to run on production machine due to reasons like version mismatch,different configuration settings etc.

- However with docker you can package application,cut-dow OS,dependencies,environment variables,third party libraries and everything an application requires into a docker image and push it on docker hub.
  
- All instructions for building an image is written into Dockerfile.

- Then you can pull image on production machine and run it as container thus preventing the above mentioned problems.
  
## Why prefer containers over VM's?

- VM is resource intesnsive as it has its own OS and takes a slice of hardware where as containers are lightweight because they are just special types of processes.
- Time taken to start a container is much less than time taken to start a VM.

### Fun Facts

- We can't run Windows 10 container on a linux machine but we can run a linux container on a Windows 10 machine.
- MacOS don't have inbuilt support for containers so docker uses a lightweight linux VM to run linux containers.

## **Linux-Basics**

 *In this repository you will see various linux commands being used as docker has its foundation built on top of linux  concepts so it is very important to fully brush up the linux concepts before proceeding further.*

- Linux is an open source operating system so it is common for us to see specialized version of linux being made time-to-time for different purposes.

- Some of the popular linux distributions are-:
  - Ubuntu
  - Debian
  - Alpine
  - Fedora
  - CentOS

- In this repository you will be studying docker with respect to ubutu linux.
  
- In case you are on a windows machine run the following command after installing docker.

    `docker run ubuntu`

- Here docker will first try to look up for image locally and then it will pull it from docker hub.

- To check if the image has successfully been pulled run the following command.
  
  `docker ps`

- To our surprise the command will not show you any container because it only shows the running containers.So use a modified version of command to see the result.

  `docker ps -a`  

- To run the container use the following command-:
    `docker run -it ubuntu`

- Now you will see the ubuntu shell opened. A shell is a program that takes our command and passes them to OS for execution.

-