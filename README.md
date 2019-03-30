# ci-cd service tree

## Requirements
Running `docker` and  `docker-compose` installation.

## Startup
- Don't forget to set a htpasswd to secure the startpage (required step to startup
`nginx` in this case). Here: `data/nginx/conf.d/nginx.htpasswd`
- Also create directories for log entries under `data/nginx/logs`
- To get the infrastructure running, execute the following 
command:
```
# Start docker-compose scenario as daemon
docker-compose up -d --no-deps --build
```

## Environments
- DevOps (base url: `*.host`)
- Integration (base url: `*.integration.host:8080`)
- Production (base url: `*production.host:8081`)

### Configuration
#### Nginx
##### Security
- nginx.htpasswd: `data/nginx/conf.d/nginx.htpasswd`

##### Access
To access a service in production and integration environment, 
use the corresponding environment base url (see Environments) and 
add the service name, like `service-name123.environment.host:port`. Rules for 
service naming:
- No underscores `_` allowed 
- Characters `a-z, A-Z`, numbers `0-9` and dash `-` allowed

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