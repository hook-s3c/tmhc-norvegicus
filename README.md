# tmhc-go-boilerplate
Super bad-ass TMHC boilerplate project.

This project can be found on https://github.com/hook-s3c/tmhc-go-boilerplate

## Overview

Pentest tool and framework for rapid, accessible development. A project for our community.

## Quickstart

### Standardized Docker environment; 

For dependencies you will need to install Docker and Docker-Compose.
Instructions can be found on the wiki.

```bash
user@host$ git clone git@github.com:hook-s3c/tmhc-go-boilerplate.git
user@host$ cd tmhc-go-boilerplate
user@host$ docker-compose up -d                        # start the container
user@host$ docker exec -t -i $(docker ps -lq) bash -l  # attach to the container to get a bash prompt
root@container$ apt-get install tzdata                 # fix for docker timezone issue
root@container$ cd /root/tmhc-go-boilerplate && make run
```

You can build, test and edit the project within the container.

#### Specs and testing;

```
user@host$ docker exec -t -i $(docker ps -lq) bash -l  # attach to the container to get a bash prompt
root@container$ cd /root/tmhc-go-boilerplate && make test
```
Now open a browser on http://localhost:8080/ and you will now see the test suite loaded.

### Baremetal;

Optionally you should be able to install all the components directly on your machine.

Dependencies;

- Go (`apt-get install golang` - Ubuntu)
- Make (`apt-get install make` - Ubuntu)


## Disclaimer

Don't use for evil, always seek permission of the owner of the platform you wish to test.
Don't do crime, the government hates competition.
