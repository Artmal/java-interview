## What is the difference between Docker Registry and Docker repository?
**Docker registry** is a service that is storing your docker images.

Docker registry could be hosted by a third part, as public or private registry, line one of the following registries: 

 - Docker Hub
 - Quay
 - Google Container Registry
 - AWS Container Registry

or you can host the docker registry by yourself.
___
**Docker repository**  is a collection of different docker images with the same name, that have different tags. Tag is alphanumeric identifier of the image within a repository.

For example see https://hub.docker.com/r/library/python/tags/. There are many different tags for the official python image, these tags are all members of the official python repository on the Docker Hub. 
