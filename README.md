# Docker Starter
Docker studies in Fedora 25



## Install with DNF
1. Make sure your existing packages are up-to-date:

        $ sudo dnf update

2. Install the Docker package:

        $ sudo dnf install docker-engine

3. Enable the service:

        $ sudo systemctl enable docker.service

4. Start the Docker daemon:

        $ sudo systemctl start docker

5. Now verify if ```docker``` is up and running:

        $ sudo docker run fedora /bin/echo Hello Docker!



## Create a docker group

1. Create the docker group:

        $ sudo groupadd docker

2. Add your user to docker group:

        $ sudo usermod -aG docker your_username

3. Log out and log back in.

4. Verify that your user is in the docker group by running docker without sudo.

        $ docker run fedora /bin/echo Hello Docker!



## Basic commands
* Verify the containers existence in execution:

        $ docker ps

* Create a container and access your interactive shell:

        $ docker run -i -t fedora /bin/bash

* List all containers

        $ docker ps -a

* Get container ID

        $ docker ps -qa

* Check container details

        $ docker stats [container_ID]

* List all images

        $ docker images

* Remove a container

        $ docker rm [container_ID]

* Set a name to new container

        $ docker run -it --name jdk8 fedora

* Commit the changes

        $ docker commit [container_ID] [image_name]

* Create self-destructive containers with `--rm` option

        $ docker run -it --rm fedora /bin/bash

* Mapping ports between host and container with `-p` option

        $ docker run -it -p 8080:80 fedora /bin/bash

* Send execution to background with `-d` option

        $ docker run -d fedora /bin/echo Hello Docker!

* Stop the container

        $ docker stop [container_name or container_ID] 

* Start the container

        $ docker start [container_name or container_ID] 

* Remove a image

        $ docker rmi [image_ID]

* Remove all containers

        $ docker rm $(docker ps -qa)

* Remove all images

        $ docker rmi $(docker images -q)

