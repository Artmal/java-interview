## Why use docker?
1. **Lightweight** 

First, docker images are usually smaller than VM images, makes it easy to build, copy, share.
Second, Docker containers can start in several milliseconds, while VM starts in seconds.

2. **Layered File System**

Images have layers, and different images can share layers, make it even more space-saving and faster to build.
If all containers use Ubuntu as their base images, not every image has its own file system, but share the same underline ubuntu files, and only differs in their own application data.


