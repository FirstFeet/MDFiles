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
    Docker stack ls
Docker Parameters
    --name
    -p
    -v
    --help
    -it
    --mount source=srcdir, target=targetdir
    -e -> to add environment variable

========================

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
        Visualizer

========================


Docker Swarn
    clusturing and Scheduling tool
    Docker native support
    Orchestration
    Two nodes
        Master node
        Worker node
    Swarm is implemented with Raft algorithm
    Raft algorithm is used for fault tolaerance
    Three roles: Leader, follower, candidate
    Handling failure: election process
    Leader: Task scheduling, Load balancing, Rolling updates, Security
    Docker Containers
        ➢ Docker Swarm : The cluster management and orchestration features embedded in the Docker Engine are built using swarmkit.
        ➢ A swarm consists of multiple Docker hosts which run in swarm mode and act as managers (to manage membership and delegation) and workers (which run swarm services).
        ➢ Host : Docker host can be a manager, a worker, or perform both roles.
        ➢ Service : When you create a service, you define its optimal state (number of replicas, network and storage resources available to it, ports the service exposes to the outside world, and more).
        ➢ Docker Swarm :Docker Swarm maintains the Service Desired State. For instance, if a worker node becomes unavailable, Docker schedules that node’s tasks on other nodes.
        ➢ Task : Task is a running container which is part of a swarm service and managed by a swarm manager.
    Initilize Docker Swarm
        docker Swarm init --advertise-addr
        Docker info - Swarn - active/inactive
        Once active we will get the Node Address and Manager Address
        Docker swarm --help
            ca, init, join, join-token, leave, unlock, unlock-key, update
        Docker service --help
            create, inspect, logs, ls, ps, rm, rollback, scale, update
    Create Service in Docker Swarm
        Docker service create
        Services has containers
        docker service ls - list all services
        docker services ps <serviceId> - list all containers
        Scale up services - docker service update <service_name> - -replicas <Number of Services>
        Delete a container - docker container rm -f <service_name>
        docker service rollback <serviceId> 
    Docker swarm cluster
         Docker playground - https://labs.play-with-docker.com/
         Manager status is  docker node ls
    Create Docker Swarm Cluster | Complete Configuration
        Digital Ocean + Docker Install
        RollOut machine on Cloud like AWS, Google, Azure, DO etc.
        Install Docker CE on Worker Nodes
        Add user to Docker Group
            sudo usermod -aG docker <username>
    Create Docker Swarm Cluster | Complete Initialization and SetUp
        Find all the Commands work on Docker Swarm Node 
            docker node --help
                Commands:
                    demote      Demote one or more nodes from manager in the swarm
                    inspect     Display detailed information on one or more nodes
                    ls          List nodes in the swarm
                    promote     Promote one or more nodes to manager in the swarm
                    ps          List tasks running on one or more nodes, defaults to current node
                    rm          Remove one or more nodes from the swarm
                    update      Update a node
        Get Token at runtime:
            docker swarm join-token manager
        Switch Manager Node in Docker
            docker node update - -role manager <node_name>
        Create Docker Service with Replicas
            docker service create --replicas <Number of Replica> <Image> <Command>
        Verify Which Node is running, which containers 
            docker service ps <service_name>
    Visualizing Cluster State using Docker Swarm Visualizer
        Executing a visualizer on Docker Swarm involves using a tool that can provide a graphical representation of your Docker Swarm cluster.
        Popular tool for this purpose is "dockersamples/visualizer"
        Write a Compose file.
        Execute Compose file as Stack on Docker Swarm. docker stack deploy -c docker-compose.yml visualizer
    Docker Swarm Networking
        

    


