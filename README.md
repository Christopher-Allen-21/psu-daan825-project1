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

## Accessing PostgrSQL from DBeaver
- Have psu-postgresql docker container running along with postgres inside the docker container
- Open DBeaver
- Click "New Database Connection"
- <img width="1356" height="945" alt="Screenshot 2026-03-12 at 9 58 32 AM" src="https://github.com/user-attachments/assets/83972c48-7a29-46f4-9a14-f32604be6255" />
- Choose PostgreSQL
- <img width="1416" height="856" alt="Screenshot 2026-03-12 at 10 00 11 AM" src="https://github.com/user-attachments/assets/d733a9ab-645c-40b1-a05a-f110b9296cb3" />
- Enter the connection settings (**make sure "Show all databases" is selected**)
- <img width="688" height="595" alt="Screenshot 2026-03-12 at 10 01 09 AM" src="https://github.com/user-attachments/assets/46e5bab2-3419-47c7-831d-edaefc3b8678" />
- After clicking Finish and installing the drivers you should see student database
- <img width="1407" height="879" alt="Screenshot 2026-03-12 at 10 02 03 AM" src="https://github.com/user-attachments/assets/06d1a22b-d535-4a9c-b673-13426803a227" />

## Create Knime Workflow
- Create a new workflow
- <img width="1706" height="948" alt="Screenshot 2026-03-13 at 9 20 23 AM" src="https://github.com/user-attachments/assets/6eeb19bc-36d3-4bbe-b157-12b56e7aa33e" />
- Drag the CSV Reader node over into drag and drop section
- <img width="857" height="476" alt="Screenshot 2026-03-13 at 9 26 12 AM" src="https://github.com/user-attachments/assets/0a9eb0d1-d862-4456-b359-56530fd7b3a6" />
- Right click on CSV Reader node and configure (I selected the relevant file and changed the delimiter from "," to "|" to match the data file). You should see a preview of the data at the bottom
- <img width="1142" height="999" alt="Screenshot 2026-03-13 at 9 30 02 AM" src="https://github.com/user-attachments/assets/2ce057d2-7610-4d1b-a142-76946db9e691" />
- Drag in a PostgreSQL Connector node into the workflow. Right click and modify the connection settings. Input hostname, database name, port, and username and password to match what we have in Docker db
- <img width="1707" height="936" alt="Screenshot 2026-03-13 at 9 33 14 AM" src="https://github.com/user-attachments/assets/2af811bf-daeb-44f4-94aa-6d2a2bc31158" />










