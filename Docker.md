Install docker
    Windows 
    mac
Virtual Machine vs Docker
Image and Containers
Docker Environment
    Docker Engine
    Docker CLI Client
    Docker buildx
    Docker Compose
    Docker content trust
    Kubernetes
    Credintial helper
Docker Ecosystem
    Docker Client
    Docker server
    Docker machine
    Docker images
    Docker Hub
    Docker Compose
    Docker engine
    Docker tag
    Docker repository
    Docker registry
    Docker Container
    Docker volumes
Docker Networking
    Bridge
    Overlay
    Container network interface
    DNS
Docker Images
    Images contains the data to run the container
    Docker images management
    Deploy docker images
    Local Images
    Docker hub central Repository - hub.docker.com
    docker pull [imagename]:[tagname]
    Image types
        base image
        child image
        official image
        User image 
    Docker image layers concept
    Docker Image tagging
    push Docker Image to cloud
    docker login
    The  docker file can be pushed to the repository  only using the suffix with the username
Docker File
    Basics
    Need for dockerfile
    Dockerfile instruction - used to create docker images
        FROM, RUN, ENV, ARG, LABEL, CMD, EXPOSE, VOLUME, COPY, ADD, WORKDIR
    Building docker Image
    -t -> is used to mention the tag name
    Docker image prune -a -> this will delete all the images that are not currently running
    docker build -t [username/tagname:version] [*dir]
    docker inspect [username/tagname:version] 
    Copy file from local to container
Data management in containers
    Volumes - Volumes will not be removed when used removes the container
    Bind mounts - can be stored any where in host system
    The location of the volume in local will be in inspect of the container
        Under Mounts -> source/destination
    --mount source=srcdir, target=targetdir
    docker volume create <name>
    Diff bet Volumes and BindMounts
    type bind - sync the bind folder with container
    Project 1 - Update mysql database version with data
    Project 2 - Update files in nginx server
    TO CHECK AND CONFIRM: Volumes transfer file from contai ner to local and Bind do it vice a versa.
Docker Compose
    Role- Single command for image building and container creation
    compose-build - docker compose build
    compose-up  - dockler compose up - will download all the images required for the container and start the containers. -d is used to run in detached mode. -f to provide filename
    compose-down - docker compose down
    docker compose version
    docker compose --help
    docker compose cp
    docker compose push
    docker compose logs [Service name]
        --tail=10
        -- follow
    execute Application in docker compose
    View container logs
    Shell into container
        docker compose exec [container] bin/bash
    Yaml files
        YAML Section tags
        container_name
        Services
        Volumes
        Environment Variable
        Networks
        Ports
        Commands
        Build
        Image
        depends_on
        If we have multiple dockerfile it is manditory to have the dockerfile name
Docker Repository
Docker Registery

Docker Commands
    Docker Build
    Docker pull [imagename] 
    Docker start [container]
    Docker stop [container]
    Docker kill [container]
    Docker container log
    Docker container top
    Docker restart/Pause
    Docker rename
    Docker push
    Docker commit
    Docker volume create/inspect/prune/rm
    Docker system prune
    Docker attach
    Docker images
    Docker ps
    Docker ls
    Docker config
    Docker inspect [container]
    Docker stat [container]
    Docker CP
    Docker Diff
    Docker save
    Docker images
    Docker Events
    Docker Export
    Docker Exec
    Docker info
    Docker Load
    Docker login/logout
    Docker logs
    Docker network
    Docker Node
    Docker plugin
    Docker rm/rmi
    Docker search
    Docker swarm
    Docker version
    Docker volume
    Docker wait
Docker Parameters
    --name
    -p
    -v
    --help
    -it
    --mount source=srcdir, target=targetdir
    -e -> to add environment variable



