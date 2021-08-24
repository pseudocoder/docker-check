# docker-check

A bash script to check whether the image used for a docker container is up-to-date relative to the source repo.

Note testing is fairly limited, it will quite likely break with new cases / formats!

### Usage

    Usage: docker-check [-?] [-q] [-v] [-a] [container] [container]
    
    Checks docker containers to confirm if their image is up-to-date relative to the repo.
    
    Options:
    -q           quiet - only report out-of-date containers
    -v           verbose
    -vv          double verbose - prints requests and outputs manifest(s) to manifest#.json
    -a           check all containers
    container    name of container to check (multiple containers can be provided)`

### Recommended Usage

Run in crontab with options -a and -q so that any output is just out-of-date repos and can be emailed as a notification.

### Supported Repos

Currently has been tested against:

* Docker Hub (default repo, hub.docker.com)
* GitHub (ghcr.io)

### Supported Manifests

Seems to work OK with both v2.1 and v2.2 manifests

