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

