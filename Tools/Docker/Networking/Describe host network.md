## Describe host network
If you use the `host` network driver for a container, that container's network stack is not isolated from the Docker host. For instance, if you run a container which binds to port 80 and you use `host` networking, the container's application will be available on port 80 on the host's IP address.

The host networking driver only works on Linux hosts, and is not supported on Mac, Windows, Windows Server.
