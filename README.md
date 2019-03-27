## Dockerized - Jenkins-CI

This Docker Compose File configures and orchestrate the provisioning of a Jenkins Server as a container.

### Prerequisites

- Docker Engine
- Docker Compose 3.7 
- Docker Swarm Mode Enabled (Optional)


### How To Run The Docker-Compose File

- Method 1 : To setup/deploy or update a jenkins-ci using a standalone docker-ce
```bash
$ docker-compose pull ; docker-compose -f docker-compose.yml -p jenkins up -d
```

- Method 2.1 : To setup/deploy a jenkins-ci using a docker-swarm cluster
```bash
$ docker stack deploy -c docker-compose.yml jenkins

```
- Method 2.2 : To update a jenkins-ci image using a docker-swarm cluster
```bash
$ docker service update --image jenkinsci/blueocean:latest jenkins_jenkins
```

### Built For/With

* [Jenkins BlueOcean Image](https://hub.docker.com/r/jenkinsci/blueocean) - Jenkins BlueOcean Image
* [Docker Compose](https://pypi.org/project/docker-compose) - Docker Compose


## Authors

* **Gerald Luzangi**
