## Why it is recommended to run only one process in a container?
1. Scaling containers horizontally is much easier if the container is isolated to a single function. Need another apache container? Spin one up somewhere else. However if my apache container also has my DB, cron and other pieces shoehorned in, this complicates things. 
2. Having a single function per container allows the container to be easily reused for other projects or purposes.
3. Is also makes it more portable and predictable for devs to pull down a component from production to troubleshoot locally rather than an entire application environment. 
4. Splitting functions out to multiple containers allows more flexibility from a security and isolation perspective. You may want(or require) services to be isolated on the network level - either physically or within overlay networks - to maintain a strong security posture or comply with things like PCI.
5. Other minor factors such as dealing with stdout/stderr and sending logs to the container log, keeping containers as ephemeral as possible etc.
