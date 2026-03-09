# psu-daan825-project1

## Docker Commands
- **docker images** - lists Docker images
- **docker ps** - lists only running Docker containers
  - **docker ps -a** - lists all Docker containers
- **docker rmi** - removes one or more specified images; ex: docker rmi <my-image>:latest
- **docker build** - builds a new Docker image from a Dockerfile and a "context" (set of files at a specific path); ex: docker build -t <my-image-name>:tag .
- **docker run** - creates and starts a new container from a specified Docker image; ex: docker run <my-image>
  - **docker run -it** - starts a container in interactive mode; ex: docker run -it <my-image>


## Introduction
Campaign finance data provides valuable insight into the dynamics of political elections. This data includes who contributes to candidates, where contributions originate, and how fundraising trends evolve over time. The Federal Election Commission (FEC) maintains detailed records of individual and organizational contributions to federal candidates. In this project, we will examine the FEC campaign finance contribution data from the 2024 election cycle for two candidates from each party using data from four states.
