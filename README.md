# ci-cd service tree

## Requirements
Running `docker` and  `docker-compose` installation.

## Startup
- Don't forget to set a htpasswd to secure the startpage (required step to startup
`nginx` in this case). Here: `./data/nginx/conf.d/nginx.htpasswd`
- To get the infrastructure running, execute the following 
command:
```
# Start docker-compose scenario as daemon
docker-compose up --build -d
```

## Environments
- DevOps (base url: `*.host`)
- Integration (base url: `*.integration.host`)
- Integration (base url: `*.host`)

### Configuration
#### Jenkins
- Base url: `jenkins.host`

##### Installation
Retrieve the initial installation password from
command line logs or access the container and open 
the named directory on the installation page.

#### Nexus
- Base url: `nexus.host`

##### Docker registry
- Base url: `docker.nexus.host`