## What is build context?
Let's start with the command used to build a Docker image:

    $ docker build [OPTIONS] PATH | URL | -
   
The build context is the set of files located at the specified PATH or URL. Those files are sent to the Docker daemon during the build so it can use them in the filesystem of the image. Let's illustrate this.
___
Once we have a Dockerfile, we can build an image using docker build, like this:

    $ docker build -t "simple_flask:dockerfile"

The final "." tells Docker to use the Dockerfile in the current directory.
