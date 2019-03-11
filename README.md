# ci-cd service tree

## Requirements
Running `docker` and  `docker-compose` installation.

## First steps
It is recommended to adjust the default passwords for the 
following services inside docker-compose.yml:
* __mysql__: `MYSQL_PASSWORD` & `MYSQL_ROOT_PASSWORD`

## Startup

To get the infrastructure running, execute the following 
command:
```
# Start docker-compose scenario as daemon
docker-compose up --build -d
```

### Configuration
#### Gitea
* URL: <http://1.2.3.4:8080>

##### Installation
Launch the Gitea installation page by accessing 
`/install` and adjust these parameters:
* __Host__: mysql:3306
* __Username__: gitea
* __Password__: see _First steps_
* __Database Name__: gitea
* __SSH Server Domain__: 1.2.3.4:8080
* __Gitea Base URL__: http://1.2.3.4:8080/

#### Jenkins
* URL: <http://1.2.3.4:8081>

##### Installation
Retrieve the initial installation password from
command line logs or access the container and open 
the named directory on the installation page.

#### Nexus
* URL: <http://1.2.3.4:8082>
