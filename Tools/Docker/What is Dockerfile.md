## What is Dockerfile?
A dockerfile is a script which contains a collection of dockerfile commands and operating system commands (ex: Linux commands).
_____

Here is the format of the `Dockerfile`:
```Dockerfile
# Comment
INSTRUCTION arguments
```

A `Dockerfile` **must start with a `FROM` instruction**. The `FROM` instruction specifies the [_Base Image_](https://docs.docker.com/engine/reference/glossary/#base-image) from which you are building. 
___
Below are some dockerfile commands you must know:
**FROM**
The base image for building a new image. This command must be on top of the dockerfile.

**MAINTAINER**
Optional, it contains the name of the maintainer of the image.

**RUN**
Used to execute a command during the build process of the docker image.

**ADD**
Copy a file from the host machine to the new docker image. There is an option to use an URL for the file, docker will then download that file to the destination directory.

**ENV**
Define an environment variable.

**CMD**
Used for executing commands when we build a new container from the docker image.

**ENTRYPOINT**
Define the default command that will be executed when the container is running.

**WORKDIR**
This is directive for CMD command to be executed.

**USER**
Set the user or UID for the container created with the image.

**VOLUME**
Enable access/linked directory between the container and the host machine.
