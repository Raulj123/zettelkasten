# What is Docker
* Docker is a virtualization software
* Packages application will all dependencies, configurations, system tools and runtime

# Images
* Application artifact
* Includes app source code, complete environment configuration 
* Add env variables, create directories, files
* What is in it
	Application -> JS app
	Any services needed -> Node
	OS layer -> Linux
* Commands
```python
docker images        # list all Docker images

# Docker run creates a new container each time
docker run {name}:{tag}  # Creates a container from a given image, starts it
docker run -d or --detach   # Runs container in background and prints id
docker run -d -p {Host_Port}:{Cont Port}or --publish # Publish a containers port to host
docker run --name web-app    #Assigns a name to container

docker logs {container}  # View logs from service running container 

```
* ## Docker Registries
	* A storage and distribution system for Docker images(Docker Hub)
```python
docker pull {name}:{tag}    # Pull image from a registry
```
* ## Image Versioning
	* Docker images are versioned 
	* Different versions are identified by tags
* ## Build Image
* builds a image from a docker file
```python
docker build {path}
docker build -t app:1.0 or --tag   # sets a name and optionally a tag in name:tag
docker build -t app-1.0 .  # Last param is location of docker file. Dot means current directory
```
# Containers
* Starts the application 
* ==A running instance of an image== 
* Can run multiple containers from 1 image
```python
docker ps          # List running containers
docker ps -a or --all  # list alll containers(stopped or running)

docker stop {conatiner}  # Stop one or more running containers(id/name)
docker start {container} # Starts one or more..
```
* Application inside container runs in an isolated Docker network
* Need to expose the container port to the host
* ### Port Binding: 
	* Bind the container port to the hosts port to make the service available

# Public and Private Docker Registries
* Docker hub is public 
* Company creates own image and don't want it to be public fam
* Called a Private Registries 
	* All big cloud providers offer private reg. 
	* Amazon ECR
	* Google Container Registry
# Registry vs Repository
* Docker Registry a service providing storage
	* Can be hosted by third party or AWS
	* In there collection of repositories
	* ## Docker Repository 
		* Collection of related images with same name but different versions

# Docker file
* create a definition on how to build an image from our app
* ### Docker files start from a base image
	* FROM
		* Docker image that your image is based on, Linux OS with w/e your image is
* ###  Need application code in container
	* COPY
		* Copies files or directories from src and adds them to the file system of the container at the path des
* ### Change into directory
	* WORKDIR
		* sets the working directory for all the following commands
		* like changing cd
* ### Execute commands
	* RUN:
		* will execute any command in a shell inside a container 
* ### Last command to start app
	* CMD
		* when a Docker container starts
		* can only be on CMD instruction in a Docker file 
```python
FROM node:{version/tag}

COPY package.json /app/           copy json to app/
COPY src /app/          slash at end of app create folder if not exist yet 

WORKDIR /app
RUN npm install

CMD ["node", "index.js"]

``` 

# How it all works 
1) Developer works on JS app
2) pushes code to git
3) Triggers a CI/CD pipe on Jenkins
4) Jenkins Builds app then Docker images
5) Pushed to a Private Repository (AWS ECR)
6) Development server pulls image from ECR