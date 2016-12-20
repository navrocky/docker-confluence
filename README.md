# Confluence docker image based on Oracle JRE

[Confluence](https://www.atlassian.com/software/confluence) is a team collaboration software. Written in Java and mainly used in corporate environments, it is developed and marketed by Atlassian.

This image is based on the officially supported Java platform (https://confluence.atlassian.com/doc/supported-platforms-207488198.html). 
  
## Simple usage

```
$ docker run --rm -v ${PWD}/data:/var/atlassian/confluence -p 8090:8090 navrocky/confluence:latest 
```

## Docker compose

```yaml
version: "2"
services:
  confluence:
    image: navrocky/confluence:latest
    ports:
      - 8090:8090
    volumes:
      - confluence_data:/var/atlassian/confluence
volumes:
  confluence_data:
```