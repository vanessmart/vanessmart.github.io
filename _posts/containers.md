---
layout: post
---

# Containers 
- What Does Containerization Mean for DevOps? 
	- Containerization entails **placing a software component and its environment, dependencies, and configuration, into an isolated unit called a container**. This makes it possible to deploy an application consistently on any computing environment, whether on-premises or cloud-based.

____
### Using Terminal to Work with Containers
**Docker:**
check for running containers:
`docker ps`

check for all containers:
`docker ps -a`


Run a Docker container:
`docker run --rm -it --name zebra ubuntu:20.04 bash`

* `--rm` : remove the container after it stops running
* `-i` : run container as interactive
* `-t` : give me a pseudo tty
* `--name` : give it a human readable name
* `ubuntu` : container we want to run
* `20.04` : version of container we want to run
* `bash`: thing we want to run in the container

____ 

* `-d` : daemonize this container (daemon = running withour expecting input - running in the background)

____

Container only exists as long as it continues to execute what we asked it to execute:
- ex: 
`docker exec -it zebra top (execute top on Zebra container)`
`> output`
`exit`

*Note - We ran the container on bash so when we tell it to exit, it quit running. Our execution of 'top' from the docker command from above ended also because the container was only set to run bash (once told to exit, it exited all 'jobs' also).*

---

### Difference between Containers & VMs
* Containers 
	* OS level
	* Isolation of the process
	* apps/processes running independently from each other


* Virtual Machines 
	* Hardware/machine level
	* Isolation of the machine
	* Machines running independently from each other



	
	

	




