After we made sure that the application is running with Docker container, you may want to use it later or on another server or even share it with others.

So we will push it to DockerHub.

To do that, you will need to expose you username and password in your pipeline, and this is not a best practice.

To do so, you will have to create Jenkins credentials, to keep your username and password secret.


If you dont have DockerHub account, do the follwoing:

1- Create one from https://hub.docker.com/signup

2- Verify your email


Then do the following to create a Jenkins credentials:

1- Click `Manage Jenkins` from the left panel.

2- Under `security` section, click `Manage Credentials`.

3- Click any domain in the `Domain` column.

4- On the top left, click `Add Credentials`.

5- For `Kind`, select `Username and Password`

6- For `Scope`, select `Global`.

7- For `Username`, type `<your-dockrhub-username>`.

8- For `Password`, type `<your-dockrhub-username>`.

9- For `ID`, type `summeracademyid`

10- Click `Save`.

Now your credentials are created, you will use this ID to recall your credentials in the pipeline.

Lets proceed with our final stage to push our image to the DockerHub.

