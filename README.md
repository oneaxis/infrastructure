# ci-cd service tree

## Requirements
Running `docker` and  `docker-compose` installation.

## Startup

To get the infrastructure running, execute the following 
command:
```
# Start docker-compose scenario as daemon
docker-compose up --build -d
```

### Configuration
#### Jenkins
* URL: <http://jenkins.1.2.3.4>

##### Installation
Retrieve the initial installation password from
command line logs or access the container and open 
the named directory on the installation page.

#### Nexus
* URL: <http://nexus.1.2.3.4>
