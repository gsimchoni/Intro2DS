# How to Install Docker

0. Create a docker account in order to install (just email & password):  

https://www.docker.com/

1. install docker:

Windows*: https://docs.docker.com/docker-for-windows/install/

Mac OS: https://docs.docker.com/docker-for-mac/install/

Linux: https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/

* Requires Windows 10. If not, install Docker Toolbox: https://docs.docker.com/toolbox/overview/
* In Windows requires restarting, might want to save your work before.

2. Run in a terminal*:

`docker version`

You should be able to see the version of docker and other details.

* Linux/Mac users do not need explanations. Windows users: this is either the command line (Win + R keys, type "cmd" and Enter), PowerShell or some other terminal you like, e.g. Cygwin, Git Bash.

If you want to use WSL in Windows 10 see here:

https://nickjanetakis.com/blog/setting-up-docker-for-windows-and-wsl-to-work-flawlessly

3. Hello-World:

`docker run hello-world`

This should download the hello-world image from [Docker Hub](https://hub.docker.com/) (the first time) and print some welcoming messages:

> Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
d1725b59e92d: Pull complete
Digest: sha256:0add3ace90ecb4adbf7777e9aacf18357296e799f81cabc9fde470971e499788
Status: Downloaded newer image for hello-world:latest
Hello from Docker!
..."

4. If `docker version` worked but `docker run hello-world` didn't: try `docker login` first to enter your account details.

5. Example for Windows/Mac users:

`docker run -ti ubuntu`

Will download the latest Ubuntu image from Docker Hub, run it and there you go, you're working in Linux!

6. See running containers:

`docker ps`

7. Stopping/removing a container:

`docker stop <container_id>`

or

`docker rm <container_id>`