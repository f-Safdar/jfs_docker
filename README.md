# jfs_docker 

This project is to build and deploy a full stack application using Docker and Heroku.

**Build and deploy code to a web hosted environment.**

**Deploy an application container to a cloud infrastructure.**

- **Docker** is a platform for developers and sysadmins to build, run, and share applications with containers.
- **Containers** are flexible, lightweight, portable, loosely coupled, scalable, and secure.

The 4 common instructions that are contained in a Dockerfile are: FROM, ADD, ENTRYPOINT

FROM says what are various base ways to build this images.Java spring boot porject using java `openJDK:18`, dont have to specify html,JS, css files , because they are running in the browser, java is not running in the browser. so we specify Java JDK 18. Java is going to be a part of containerization.

>The FROM instruction specifies the Parent Image from which you are building

>According to Official Docker Documentation the MAINTAINER instruction is deprecated. Instead, one should use the LABEL instruction to define the author of the generated images.

>The LABEL instruction is more flexible, enables setting metadata, and can be easily viewed with the command docker inspect.

Add our jar file which we created using ADD command and give alias to know Hey Docker!! know this files as `jfs_docker.jar`.

*The ADD command is used to copy files/directories into a Docker image*

ENTRYPOINT is "starting main file", it is used in diff context in s/w  or web development generally.It says where is the default place that you want to run, whether it is docker for example,

if building something where is the file you want to run and how do you want to run it.so a entrypoint run as this command `['java', 'jar', 'jfs_docker.jar']` using docker

>The ENTRYPOINT instruction is used to set executables that will always run when the container is initiated
