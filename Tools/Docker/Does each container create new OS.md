## Does each container create new OS?
Docker uses host OS kernel, there is no custom or additional kernel inside container. All containers which run on a machine are sharing this "host" kernel.
