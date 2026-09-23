# jenkins-docker-compose

# Jenkins + Docker-in-Docker (ISEC6000 Assessment 2)

Docker Compose setup for a Jenkins CI server that builds Docker images through a TLS-secured DinD daemon.

## Layout
- `docker-compose.yml`: Jenkins and DinD services, volumes and network
- `jenkins/Dockerfile`: Jenkins LTS image with the Docker CLI and pipeline plugins
- `docs/`: notes and evidence

## Run
    docker compose up -d --build

Jenkins listens on 127.0.0.1:8080 only. Reach it through an SSH tunnel.
