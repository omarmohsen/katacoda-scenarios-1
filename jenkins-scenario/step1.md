You are going to run Jenkins on a Docker container on the host.

Dell's DevOps team already created a Jenkins Docker image, so you can use it in our scenario.

Execute the following command to run the Jenkins Docker container:

`docker run -d -u root --name jenkins \
    -p 8080:8080 -p 50000:50000 \
    -v /root/jenkins:/var/jenkins_home \
    omarmohsen/jenkins-sa
`{{execute}}


Meaning of the parameters used in the `docker run` command:

`-d` --> runs in the background

`--name` --> name of the container running

`-p` --> the port number where you can access the container

`-v` --> the volume attached to the Jenkins container


Now lets check that our container is running

`docker ps`{{execute}}

You can view the logs of the container to check that Jenkins in up and running:

`docker logs jenkins -f `{{execute}}

Enter CTRL+C after ensuring that Jenkins is up.

In the next steps, you'll use the Jenkins dashboard to configure the plugins and start building the Pipeline.
