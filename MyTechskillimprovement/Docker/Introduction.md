Problems

	Ø Deployments are way too complicated these days

		There are multiple languages,frameworks,databases,dependencies,dev environment,pro,qa and staging 
		Even before starting you will get confusion where you're gonna deploy things.
		
	
	
	Docker run [image name] -- To pull image from docker hub and start running.
	Docker run [image name : version] -- To pull image from docker hub and start running
	Docker ps -- To check running processes.
	Docker images 	To check all the images in laptop
	Docker ps	To check all running processes/images
	Docker run [image name]	To pull image from docker hub and start running
	Docker run [image name:version]	To pull image from docker hub and start running
	Docker run -d redis	To get ID of the container and start in detach mode
	Docker stop [container id]	To stop the container
	Docker start [container id]	To start the container
	Docker ps -a	To list all the running and stopped container
	Docker run -p[host port:container port imagename]	,To do binding between host port and container port
	Docker logs [containerid/containername]	To check logs of the container
	Docker run -d -p[hostport:containerport ] --name  [nameofourchoice] imagename	To choose a specific name instead of default name for the container
	Docker exec -it [containerid] /bin/bash	To get inside the containere to check config files and manymore details related to that particular container
		
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	Ø What is docker ? What is containter ?t
	Overview :
	Ø What is container and what problems does it solve ?
	      >> what is container ?
				--> A way to package application with all the necessary dependencies and configuration.
				--> portable artifact, easily shared and moved around
				--> Makes development and deployment more efficient
			-- A layer of images
			-- Mostly linux base image, because small in size
			-- Application image on top
			
	       >> Where do containers live ?
			§ They live in a container repository
			§ Some companies have their own private repositories
			§ Public repository for docker named Docker hub
			
	Ø Container Repository
	Ø DEVELOP application
	  In Application Development,
		○ Before Containers
			§ Installation process different on each OS environment
			§ Many Steps where something could go wrong
	
	Developer sends artifact to the operations team to configure & deploy.
				□ Configuration on the server needed
					® Dependency version conflicts
					® Misunderstandings between developers and operations team
				□ Textual guide of instructions
				
		○ After containers
	        >> own isolated environment
		>> Packaged with all needed configuration
		>> one command to install the app
	     Developers and operations work together to package the application in a container
	Ø No environmental configuration needed on server --except Docker runtime.
		
		Docker Image 	Docker Container
		It is the actual package	Actually start the application
		Configuration-->version-->start script
		Artifact, that can be moved around	Container environment is created.
		Not running then it's image	Running it's container
	Ø Having different layers helps to reduce time when we install same image from different version
	Ø Docker vs vitualmachine
		○ Dockere on OS level
			§ How OS works
				□ OS consists of two layers namely kernel and application on top of hardware
					® Kernel communicates with the hardware of computer like CPU,RAM etc
					® They use same linux kernel but implemented different application on top.
			§ Both docker and virtual machine are virtualization tools
		○ Different levels of abstraction
		○ Why linux based docker containers don't run on windows
	Docker 	Virtual Machine
	Virtualization tool	Virtualization tool
	Virtualizes application layer and depends on host for kernel layer	Virtualizes complete os. It has their own oskernel
	Size of docker images is smaller because they just have to implement one layer. Image size In megabytes	Size of virtual machine is bigger . Size is in gigabytes.
	Speed : docker containers run faster because there is no need to put os kernel	Little bit slower due to every startup they need to start running os
	Compatability : You can run only any linux distribution	It is compatible with all os 
	Ø 
	Ø DEPLOY application
	
	Ø Docker vs virtual machine
	Ø Docker installation
		Go through the offical docker documentation on getting instructions of how to install docker on your machine locallyl
	Ø Main commands
		○ Containers vs images
		○ Containers	Images
		It is the running environment for image	
		It has filesystem, environment configs, application image(postgres,redis etc)	
		Port : 5000 which talks to application running inside of a container	
		Virtual file system	
		Container port vs host port
		Ø Multiple containers can run on your host machine
		Ø Your laptop has only certain ports available
		Ø Conflict when same port on host machine
		We need to do binding between host port and container port inorder to use container.
					
		○ Version and tag
		○ Docker commands
		
	Ø Debugging a container
			§ Docker run Is where you create a new container from an image[To create new container]
			§ Docker start you work with containers instead of images. [To restart existing container]
			
		Workflow with docker
		>> development-->ci/cd-->deployment
		
			Docker pull mongo --to get mongodb database
			Docker pull mongo-express
			Docker images
			Docker Network :
			Ø Docker network ls --To check already having network
			Ø Docker network create mongo-network [To make network connection with mongodb]
			Ø Docker network ls
			Ø Docker run -p 27017:27017 -d -e MONGO_INITDB_ROOT_USERNAME=admin -e MONGO_INITDB_ROOT_PASSWORD=password --name mongodb --net mongo-network mongo
		Docker logs <containerid> --to check status of container
		
		Docker run -d\ --To run containers in detached mode
		Docker run -p 8881:8881 -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin -e ME_CONFIG_MONGODB_ADMINPASSWORD=password --net mango-network --name mongo-express -e ME_CONFIG_MONGODB_SERVER=mongodb mongo-express
		
		Docker logs <container id>
		Docker ps
		
	Ø Volume - persiststant data
	Ø Developing with containers
	Ø Docker compose - running multiple services
	Ø Docker file --building your own docker image
	Ø Private docker repository (AWS)
	Ø Deploying the containerized app
	Ø Volumes Demo
+

