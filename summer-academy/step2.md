In this step we are going to run the Dockerfile to build our image

In this image we will add the hello-world application in it and we will expose a port so you can check it out and see the results yourself

First you will have to go to the clonned directory `cd hello-world-python`{{execute}}

Then make sure that Docker is running `systemctl start docker`{{execute}}

Execute `docker build -t summer-academy-hello-world:latest .`{{execute}} to build your image

Now you can see the built image through this command `docker images | grep summer-academy-hello-world`{{execute}}