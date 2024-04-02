# Overview
Repertoire is a suite of tools providing services for Reporting and ETL. 

For more infomation on Elixir Repertoire, you may visit https://docs.elixirtech.com/Repertoire/2024.0/index.html or www.elixirtech.com


# Run Repertoire with Docker Compose

## Requirement
-  Unix OS as macOS or Linux - scripts use sh or bash unix shell. You will need to adapt the scripts to other operating system as Windows
- Docker engine with Compose, you can install the software from https://docs.docker.com/get-docker/
- Elixir Repertoire trial licence is shipped with the image. You can obtain a full licence from sales@elixirtech.com and deploy via browser into the Repertoire Store or  place in "etc" folder and enable the volume mapping in docker-compose.yaml to use a local licence in the folder. 


## Steps
- Run docker compose to start and Repertoire. 

```
./run-repertoire-compose.sh 
```

This will pull a latest Repertoire image at elixirtech/elixir-repertoire docker repository, start Repertoire services.  You can use the browser to access the url as http://localhost:1730. 


## Configuration
- Docker compose configuration file is docker-compose.yaml. It is configured to run a Repertoire container. 

- Repertoire configuration parameters for Ambience is in a hidden file ".env". The parameters as

```
externalhost="localhost"
externalport="1730"
externalprotocol="http:"
```

You can configure external host, port and http protocol (http: or https:). 

##  Useful docker compose commands and scripts

Below is a list of commonly use docker command

- List the services as

```
docker compose ps
```

- To stop you can run 

```
docker compose stop
```

- To remove the containers 

```
docker compose rm
```

- To restart the containers 

```
docker compose restart
```