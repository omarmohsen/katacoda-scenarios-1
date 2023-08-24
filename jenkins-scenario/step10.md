After we made sure that the application is running with Docker container, you may want to use it later or on another server or even share it with others.

So we will push it to DockerHub.

To do that, you will need to expose you username and password in your pipeline, and this is not a best practice.

To do so, you will have to create Jenkins credentials, to keep your username and password secret.


If you don't have DockerHub account, follow these teps:

1- Create one from https://hub.docker.com/signup

2- Verify your email


Then do the following to create a Jenkins credentials:
1- Go to `Dashboard` from the left panel.

2- Click `Manage Jenkins` from the left panel.

3- Under `security` section, click `Manage Credentials`.

4- Click on (global) domain in the `Domain` column.

5- On the top left, click `Add Credentials`.

6- For `Kind`, select `Username and Password`

7- For `Scope`, select `Global`.

8- For `Username`, type `<your-dockrhub-username>`.

9- For `Password`, type `<your-dockrhub-username>`.

10- For `ID`, type `summeracademyid`

11- Click `Save`.

Now your credentials are created, you will use this ID to recall your credentials in the pipeline.

Lets proceed with our final stage to push our image to the DockerHub.
