# Ad-Hoc Doc

Various Linux distributions available for interactive use within docker.

## Why?

I'm using a lot of mac OS and Windows these days, but various tools and scripts are easier to get going, or just plain available, on Linux. Since I already have docker running on my laptop, why spin up another dedicated, resource-consuming Linux VM when I can use an interactive session in a container instead?

## How to use

You need docker-compose installed. To start up, run:

```
docker-compose run --rm TARGET
```

where `TARGET` is one of the distributions listed below.

When you run these, the directory ./scratch is mounted as a volume on /scratch in the container, so you are able to share files in and out.

## Distributions

Current distributions in the docker-compose file are split into two categories: those that run as UID 0, and those that run as a non-root user (hard-wired to UID 1000).

* Root access
    * Kali - rolling latest
    * Ubuntu - 20.04
* Regular user access
    * Ansible - Alpine based with ansible pre-installed
