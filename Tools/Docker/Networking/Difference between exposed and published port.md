## Difference between exposed and published port
**Exposed ports** can be accessed by other containers in the same docker host but they cannot be accessed publicly over the internet.

You expose ports using the `EXPOSE` keyword in the Dockerfile or the `--expose` flag to docker run. **Exposing ports is a way of documenting which ports are used, but does not actually map or open any ports. Exposing ports is optional**.
___
**Published ports** are exposed ports that are accessible publicly over the internet. Published ports are published to the public-facing network interface in which the container is running on the node(host).
