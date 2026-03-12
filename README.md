# psu-daan825-project1

## Docker Commands
- **open -a Docker** - open Docker desktop to run docker commands locally
- **docker images** - lists Docker images
- **docker ps** - lists only running Docker containers
  - **docker ps -a** - lists all Docker containers
<br><br>
- **docker build -t `<`my-image-name:tag`>` .** - builds a new Docker image from a Dockerfile and a "context" (set of files at a specific path)
- **docker rmi `<`my-image`>`:latest** - removes one or more specified images
<br><br>
- **docker run `<`my-image`>`** - creates and starts a new container from a specified Docker image
  - **docker run -it `<`my-image`>`** - creates and starts a new container in interactive mode
- **docker start `<`my-containter-id`>`** - starts a previously created container
- **docker exec -it `<`my-containter-id`>`/bin/bash** - open a bash terminal in an already running container
- **exit** - closes terminal session if at the container shell (if prompt looks like "postgres@0e857eadc3dc:/$")
- **docker stop `<`my-container-id`>`** - stops a container
- **docker rm `<`my-container-name-or-id`>`** - deletes a container



## Running PostgreSQL in Docker Container
- **docker exec -i -t `<`my-container-id`>` bash** - get bash access in running container
- **psql -h localhost -p 5432 -d student -U student –-password** - connect to postgresql (I am using "student" as the password)
- **\list** - get a list of databases
- **\q** - quits psql if inside the PostgreSQL client (if prompt looks like "psql=#" or "postgres=#")


## Introduction
Campaign finance data provides valuable insight into the dynamics of political elections. This data includes who contributes to candidates, where contributions originate, and how fundraising trends evolve over time. The Federal Election Commission (FEC) maintains detailed records of individual and organizational contributions to federal candidates. In this project, we will examine the FEC campaign finance contribution data from the 2024 election cycle for two candidates from each party using data from four states.
