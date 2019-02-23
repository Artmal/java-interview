## Describe bridge network
The bridge driver creates a private network internal to the host so containers on this network can communicate. External access is granted by exposing ports to containers. Docker secures the network by managing rules that block connectivity between different Docker networks.

In terms of Docker, a bridge network uses a software bridge which allows containers connected to the same bridge network to communicate, while providing isolation from containers which are not connected to that bridge network.
___ 
**Default bridge network(docker0)**  
The default bridge network is considered a legacy details of Docker and is not recommended for production use. Configuring is is a manual operation, and it has technical shortcomings.

Containers connected to the default bridge network can communicate, but only by IP address, unless they are linked using legacy --ling flag.
___
**Used-defined bridges**  
Containers connected to the same user-defined bridge network automatically expose all ports to each other, and no ports to the outside world.
